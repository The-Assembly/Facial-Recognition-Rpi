# Facial Recognition using Raspberry PI

## Introduction to Today's Workshop

Facial Recognition is one of the most common uses of Pattern Recognition and is AI at its most common form. A facial recognition system is most used for security purposes, with the most advanced version being launched by Smartphone manufacturers in recent months. <br/>

### Examples of Facial recognition application in use
#### Facial motion capture <br/>

Facial motion capture is the process of electronically converting the movements of a person's face into a digital database using cameras or laser scanners. This database may then be used to produce CG (computer graphics) computer animation for movies, games, or real-time avatars. Because the motion of CG characters is derived from the movements of real people, it results in more realistic and nuanced computer character animation than if the animation were created manually. <br/>

<p align="center">
  <img src="http://kinectic.net/wordpress/wp-content/uploads/2013/11/avatar_sagar.jpg">
</p>

#### Iphone X <br/> 

Apple released the iPhone X in 2017, advertising face recognition as one of it’s primary new features. The face recognition system in the phone is used for device security. The new model of iPhone sold out almost instantly, proving that consumers now accept facial recognition as the new gold standard for security. <br/>

<p align="center">
  <img src="https://km.support.apple.com/library/content/dam/edam/applecare/images/en_US/social/ios11-iphone-x-face-id-social-card.jpg">
</p>

#### Social media <br/>

**Facebook:** Beginning in 2010, Facebook began implementing facial recognition functionality that helped identify people whose faces may be featured in the photos that Facebook users update daily. While the feature was instantly controversial with the news media, sparking a slew of privacy-related articles, Facebook users at large did not seem to mind. Having no apparent negative impact on the website’s usage or popularity, more than 350 million photos are uploaded and tagged using face recognition each day. <br/>

<p align="center">
  <img src="https://www.classaction.org/media/3278.jpg">
</p>


**Snapchat:** At the most basic level, the app uses computer vision to spot you based on contrast patterns typically seen in and around a human face; however, that’s not specific enough to identify, for example, the border of your lips or where to put that dog nose. To get to that level of specificity, Snapchat trained the system using hundreds (quite possibly thousands) of faces that were manually marked with points to show where the borders of lips, eyes, nose, and face are. <br/>

<p align="center">
  <img src="https://assets3.thrillist.com/v1/image/1717288/size/tmg-facebook_social.jpg">
</p>

## Circuit assembly 

- For the servo, connect the signal line to GPIO 18 of the Raspberry Pi. To power the servo I connected a 4x AA battery pack as a power source--connecting the servo to the Pi's 5 volt output could cause problems from noise or excessive current drawn by the servo. 
- The push button is attached to GPIO 25 of the Raspberry Pi, with a 10 kilo-ohm pull-up resistor to 3.3 volt power from the Pi.

See the diagram below for how to wire the push button and servo to the Raspberry Pi.<br/>
![circuit diagram](https://user-images.githubusercontent.com/32713072/36054091-0dff02a4-0e0e-11e8-907a-8c76be8e8e0e.png)

## Installing openCV and other libraries

### Expand filesystem
If you’re using a brand new install of Raspbian Jessie, then the first thing you should do is ensure your filesystem has been expanded to include all available space on your micro-SD card.

On the terminal type:  
```
sudo raspi-config
```
Select the first option “1. Expand Filesystem”, arrow down to “Finish”, and reboot your Pi. <br/>
After rebooting, your filesystem will have be expanded to include all available space on your micro-SD card.

### Installing dependencies

First, we need to update and upgrade our existing packages:
```
sudo apt-get update
sudo apt-get upgrade
```

Install our developer tools:
```
$ sudo apt-get install build-essential cmake pkg-config
```

Let’s grab the image I/O packages and install them:
```
$ sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
```

Along with some video I/O packages:
```
$ sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
$ sudo apt-get install libxvidcore-dev libx264-dev
```

We’ll need to install the GTK development library for OpenCV’s GUI interface:
```
$ sudo apt-get install libgtk2.0-dev
```
Let’s also pull down a couple routine optimization packages leveraged by OpenCV:
```
$ sudo apt-get install libatlas-base-dev gfortran
```

Lastly, let’s install the Python 2.7 headers so wen can compile our OpenCV + Python bindings:
``` 
sudo apt-get install python2.7-dev
```
### Grab the OpenCV source

At this point, all of our dependences have been installed, so let’s grab the 3.0.0  release of OpenCV from GitHub and pull it down:
```
$ cd ~
$ wget -O opencv.zip https://github.com/Itseez/opencv/archive/3.0.0.zip
$ unzip opencv.zip
```

Let’s also grab the opencv_contrib repository as well:
```
$ wget -O opencv_contrib.zip https://github.com/Itseez/opencv_contrib/archive/3.0.0.zip
$ unzip opencv_contrib.zip
```

It’s especially important to grab the ```opencv_contrib```  repo if you want access to SIFT and SURF, both of which have been removed from the default install of OpenCV.

Now that``` opencv.zip ``` and ```opencv_contrib.zip``` have been expanded, let’s delete them to save space:
```
$ rm opencv.zip opencv_contrib.zip
```

### Setup Python
The first step in setting up Python for the OpenCV build is to install pip , a Python package manager:
```
$ wget https://bootstrap.pypa.io/get-pip.py
$ sudo python get-pip.py
```

Let’s also install virtualenv  and virtualenvwarpper , allowing us to create separate, isolated Python environments for each of our future projects:
```
$ sudo pip install virtualenv virtualenvwrapper
$ sudo rm -rf ~/.cache/pip
```

To complete the install of virtualenv  and virtualenvwrapper , open up your ```~./profile``` :
```
$ nano ~/.profile
```

And append the following lines to the bottom of the file:
```
# virtualenv and virtualenvwrapper
export WORKON_HOME=$HOME/.virtualenvs
source /usr/local/bin/virtualenvwrapper.sh
```

Now, source  your ~/.profile  file to reload the changes:
```
$ source ~/.profile
```

Let’s create a new Python virtual environment appropriately named cv :
```
$ mkvirtualenv cv
```

The only requirement to build Python + OpenCV bindings is to have NumPy installed, so let’s use pip  to install NumPy for us:
```
$ pip install numpy
```
### Compile and install OpenCV for the Raspberry Pi Zero
We are now ready to compile and install OpenCV. Make sure you are in the cv  virtual environment by using the workon  command:
```  
$ workon cv
```

And then setup the build using CMake:
```
$ cd ~/opencv-3.0.0/
$ mkdir build
$ cd build
$ cmake -D CMAKE_BUILD_TYPE=RELEASE \
    -D CMAKE_INSTALL_PREFIX=/usr/local \
    -D INSTALL_C_EXAMPLES=ON \
    -D INSTALL_PYTHON_EXAMPLES=ON \
    -D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib-3.0.0/modules \
    -D BUILD_EXAMPLES=ON ..
```

Now that the build is all setup, run make  to start the compilation process (this is going to take awhile, so you might want to let this run overnight):
```
$ make
```

Assuming OpenCV compiled without error, you can install it on your Raspberry Pi Zero using:
```
$ sudo make install
$ sudo ldconfig
```
### Finishing the install

Provided you completed the previous step without an error, your OpenCV bindings should now be installed in ```/usr/local/lib/python2.7/site-package``` :
```
$ ls -l /usr/local/lib/python2.7/site-packages
total 1640
-rw-r--r-- 1 root staff 1677024 Dec  2 08:34 cv2.so
```

All we need to do now is sym-link the ```cv2.so```  file (which are our actual Python + OpenCV bindings) into the ```site-packages```  directory of the``` cv```  virtual environment:
```
$ cd ~/.virtualenvs/cv/lib/python2.7/site-packages/
$ ln -s /usr/local/lib/python2.7/site-packages/cv2.so cv2.so
```

### Verifying your OpenCV install

All that’s left to do now is verify that OpenCV has been correctly installed on your Raspberry Pi Zero.<br/>
Whenever you want to use OpenCV, first make sure you are in the ```cv```  virtual environment:
```
$ workon cv
```
And from there you can fire up a Python shell and import the OpenCV bindings:
```
$ workon cv
$ python
>>> import cv2
>>> cv2.__version__
'3.0.0'
>>>
```
Or you can execute a Python script that imports OpenCV.<br/>

Once OpenCV has been installed, you can remove both the opencv-3.0.0  and opencv_contrib-3.0.0  directories, freeing up a bunch of space on your filesystem:
```
$ rm -rf opencv-3.0.0 opencv_contrib-3.0.0
```

### Errors in installation
If there are any errors after compiling the code above, where its suggests:
```ImportError: No module named cv2```
There could be two solutions:
-Either install openCV through python, by typing:
```
sudo apt-get install python-opencv
```
- or try redoing all the above mentioned steps.

### Setting up the GPIO pins on a Raspberry PI
The newest version of Raspbian has the RPi.GPIO library pre-installed. You’ll probably need to update your library, so using the command line, run:
- sudo apt-get install rpi.gpio
If it isn’t already installed it will be installed. If it is already installed it will be upgraded if a newer version is available.
#### Using the RPi.GPIO Library
Now that you’ve got the package installed and updated, let’s take a look at some of the functions that come with it. Open the Leafpad text editor and save your sketch as “myInputSketch.py”. From this point forward, we’ll execute this script using the command line:

- sudo python myInputSketch.py

All of the following code can be added to this same file. Remember to save before you run the above command. To exit the sketch and make changes, press Ctrl+C.

To add the GPIO library to a Python sketch, you must first import it: <br/>
```python
import RPi.GPIO as GPIO
```

Then we need to declare the type of numbering system we’re going to use for our pins: <br/>
```python
#set up GPIO using BCM numbering
GPIO.setmode(GPIO.BCM)
#setup GPIO using Board numbering
GPIO.setmode(GPIO.BOARD)
```
#### Examples: 
https://thepihut.com/blogs/raspberry-pi-tutorials/27968772-turning-on-an-led-with-your-raspberry-pis-gpio-pins <br/>
https://www.raspberrypi-spy.co.uk/2012/05/install-rpi-gpio-python-library/

### Setting up the program to run on terminal, after boot
A simple way to see how you can setup to run python file on Raspberry Pi startup (using the terminal).

- Save the python file on home/pi
- On the terminal, navigate to  /home/pi
- now open a hidden file  .bashrc  ( type "sudo nano .bashrc" on terminal and press enter)
- At the end of the file type "python" followed by your file name (eg: python3 speechtotext)
- If you want the terminal to revert back to its normal format, either comment out the command on the .bashrc file or remove it (you can access the bash file in /home/pi).

## Coding and Software implementation 

### Training the software 

This project uses the eigenfaces algorithm in OpenCV to perform face recognition. To use this algorithm you'll need to create a set of training data with pictures of faces that are and are not allowed to open the box.<br/>

Included in the project is a large set of face images that are tuned for training with the face recognition algorithm. This is the database of faces published by research AT&T Laboratories Cambridge in the mid 90's. These faces make up the set of negative images which represent faces that are not allowed to open the box. You can see these images in the **training/negative** subdirectory of the project.<br/>

To generate images of the person who will be allowed to open the box, or positive training images, you can use the included capture-**positives.py** script. This script will take pictures with the box hardware and write them to the **training/positive** sub-directory (which will be created by the script if it does not exist).

With the box hardware assembled and powered up (servo power is not necessary for this step), connect to the Raspberry Pi in a terminal session and navigate to the directory with the project software. Execute the following command to run the capture positive script:
```
sudo python capture-positives.py
```
After waiting a few moments for the script to load, you should see the following instructions:
```
Capturing positive training images.
Press button or type c (and press enter) to capture an image.
Press Ctrl-C to quit.
```
The script is now ready to capture images for training. If you see an error message, make sure OpenCV and the software dependencies from the previous step are installed and try again.<br/>

Point the box's camera at your face and press the button on the box (or send the letter 'c' in the terminal session) to take a picture. If the script detects a single face, it will crop and save the image in the positive training images sub-directory. If the script can't detect a face or detects multiple faces, an error message will be displayed.<br/>

If see error messages about not detecting a single face, you can examine the full picture that was captured by the camera to understand if it's picking up your face (or if other faces might be in view--be careful, even photos or posters with faces behind you can be detected!). Open the file capture.pgm (located in the directory with the scripts) in an image editor to see the last image that was captured. It's easiest to use a tool like Cyberduck to view the files on your Raspberry Pi over SFTP (SSH file transfer protocol).<br/>

Using the **capture-positives.py** script, capture some pictures of the face that is allowed to open the box. Try to take pictures of the face with different expressions, under different lighting conditions, and at different angles.<br/>

Once you've captured a number of positive training images, you can run the train.py script to perform the training. If it's still running, exit the **capture-positives.py** script by pressing Ctrl-C in the terminal session. Run the following python script to train the face recognition model:
```
python train.py
```
Note that this command does not need to be run as root with sudo because none of the Pi GPIO/hardware is accessed.<br/>

You should see a message that the training images were loaded, and the text ```'Training model... to indicate the training calculations are being performed. Training the face recognition model on the Pi will take about 10 minutes.```<br/>

Once the training is complete you should see the message ```'Training data saved to training.xml'. The training data is now stored in the file training.xml, which will be loaded by the box software to configure the face recognition model.```<br/>

If you're curious you can examine images that are output by the training to visualize the eigenfaces of the model. Open the **mean.png**, **positive_eigenface.png**, and **negative_eigenface.png** files in an image viewer.<br/>

The positive eigenface is a summary of the features that differentiate my face from the average or mean face. This face will be allowed to unlock the box.<br/>

The negative eigenface represents all the other faces in the training set. This face will not be allowed to unlock the box.
With the training.xml file generated, you're ready to move on to configure the servo latch and software for the project.<br/>

With the training.xml file generated, you're ready to move on to configure the servo latch and software for the project. <br/>

### Implementing a lock opening mechanism 

To run the box software, make sure the hardware is assembled and the training is complete. First you'll run the box with only power to the Raspberry Pi and not the lock servo--this will allow you to test the face recognition without locking yourself out of the box. Apply power to just the Raspberry Pi (and not the servo), then connect to the Pi in a terminal session, navigate to the folder with the software, and execute the following command:
```
sudo python box.py
```
You should see the box software load and the message ```'Loading training data...'``` appear. It should take a few minutes for the training data to load and the following message to appear:
```
Running box... 
Press button to lock (if unlocked), or unlock if the correct face is detected. 
Press Ctrl-C to quit. 
```
The box will lock itself (however because no power is applied to the servo, the lock latch should not move) and be ready to try unlocking with face recognition. Aim the box camera at your face, like you did when training the face recognition model, and press the button on the box. You should see a message that the button was pressed, and after a moment if the face is recognized you will see a message like:
```
Predicted POSITIVE face with confidence 1321.35253959 (lower is more confident). Recognized face! 
```
If the face is not recognized you will see a message like:
```
Predicted NEGATIVE face with confidence 3987.76625152 (lower is more confident). Did not recognize face!
```
If a single face couldn't be detected (because none is visible, or there are multiple faces detected) an error message will be displayed like with the training script.

When a face is found, you'll notice the prediction message includes how the face was recognized (i.e. matching either the positive or negative training data), and the confidence of the recognition. The confidence is a value like 1321.35 or 3987.77 above and represents the distance of the captured face from the predicted face--a lower distance value means the captured face is more similar to the predicted face.

To unlock the box, a captured face must be a positive prediction with a confidence value below the POSITIVE_THRESHOLD configuration value. By default the POSITIVE_THRESHOLD is 2000, so the positive prediction with confidence 1321.35 was considered a match and would have unlocked the box.

When the box is in an unlocked state, press the button to lock the box again. You do not need to have a face recognized to lock the box.

Play with unlocking and locking the box to see what prediction and confidence you get from your trained face recognition model. Ideally you want images of the positively trained face to be predicted as positive images with a low number for the confidence value. The eigenfaces recognition algorithm is sensitive to the lighting and orientation of your face, so try to have as similar conditions as when the positive training images were captured (or consider re-training your model to include more varied images).

Based on how the face recognition responds, you might consider training it again or adjust the POSITIVE_THRESHOLD configuration to a higher/lower value. 

When you're happy with how the recognition is working, apply power to the servo and try locking and unlocking the box for real. Congratulations on building the face recognition treasure box!

If for some reason your box is locked and will not recognize a face to unlock itself, you can manually set the servo position to an unlocked value by following the steps in the servo configuration. If you don't have access to the Raspberry Pi terminal or the servo isn't moving, unfortunately you'll need to disassemble your box (this is why it's a good idea to use a box with hinges on the outside!).



















