# Facial Recognition using Raspberry PI

<!doctype html>
<html lang="en-US">
<head>
<meta charset="utf-8">
<link rel="mask-icon" href="/assets/adafruit_favicon-d77f206e6cc65b40101b6e5b8987f7c35cb6a283ea73c0adad50c37f7347c61a.svg" color="#000000">
<link rel="shortcut icon" type="image/x-icon" href="/assets/favicon-0c79bd4bc582e6d4cf3afe417bd1e28120527c09d92c08a6464690c5bf6b85f4.ico" />
<title>Overview | Raspberry Pi Face Recognition Treasure Box | Adafruit Learning System</title>
<meta name="csrf-param" content="authenticity_token" />
<meta name="csrf-token" content="vPXR9ozu7WJAs/31i8igVo9Z2I1CvmwVcMAg22bDO/2FVOgQpf4C26OTUEgmsQPuDtbaksEUO/XIc2wxDmaieA==" />
<link rel="alternate" type="application/atom+xml" title="ATOM" href="/feed" />
<link rel="alternate" type="application/rss+xml" title="RSS" href="/feed.rss" />
<link rel="stylesheet" media="screen" href="/assets/application-369a01db64cf610c56e936b852f163490a5cefa648b7cbde72b1f5547b9a5af2.css" />

<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
  new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
  j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
  'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
  })(window,document,'script','dataLayer','GTM-PRPXBQ6');</script>

<meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1, maximum-scale=1">
<meta name="guide-title" content="Raspberry Pi Face Recognition Treasure Box">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:site" content="@adafruit">
<meta name="twitter:title" content="Raspberry Pi Face Recognition Treasure Box">
<meta name="twitter:description" content="Create a box that only opens when the right person looks at it!">
<meta name="twitter:image:src" content="https://cdn-learn.adafruit.com/guides/images/000/000/480/medium800/DSC00396.jpg">
<meta name="twitter:domain" content="https://learn.adafruit.com">
<link rel="canonical" href="https://learn.adafruit.com/raspberry-pi-face-recognition-treasure-box/overview" />
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
<script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","errorBeacon":"bam.nr-data.net","licenseKey":"308175db61","applicationID":"54271218","transactionName":"cVZXRUFeWghRShtEVlVcSh5AWVkT","queueTime":0,"applicationTime":278,"agent":""}</script>
<script type="text/javascript">window.NREUM||(NREUM={}),__nr_require=function(e,t,n){function r(n){if(!t[n]){var o=t[n]={exports:{}};e[n][0].call(o.exports,function(t){var o=e[n][1][t];return r(o||t)},o,o.exports)}return t[n].exports}if("function"==typeof __nr_require)return __nr_require;for(var o=0;o<n.length;o++)r(n[o]);return r}({1:[function(e,t,n){function r(){}function o(e,t,n){return function(){return i(e,[f.now()].concat(u(arguments)),t?null:this,n),t?void 0:this}}var i=e("handle"),a=e(2),u=e(3),c=e("ee").get("tracer"),f=e("loader"),s=NREUM;"undefined"==typeof window.newrelic&&(newrelic=s);var p=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],d="api-",l=d+"ixn-";a(p,function(e,t){s[t]=o(d+t,!0,"api")}),s.addPageAction=o(d+"addPageAction",!0),s.setCurrentRouteName=o(d+"routeName",!0),t.exports=newrelic,s.interaction=function(){return(new r).get()};var m=r.prototype={createTracer:function(e,t){var n={},r=this,o="function"==typeof t;return i(l+"tracer",[f.now(),e,n],r),function(){if(c.emit((o?"":"no-")+"fn-start",[f.now(),r,o],n),o)try{return t.apply(this,arguments)}catch(e){throw c.emit("fn-err",[arguments,this,e],n),e}finally{c.emit("fn-end",[f.now()],n)}}}};a("setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(e,t){m[t]=o(l+t)}),newrelic.noticeError=function(e){"string"==typeof e&&(e=new Error(e)),i("err",[e,f.now()])}},{}],2:[function(e,t,n){function r(e,t){var n=[],r="",i=0;for(r in e)o.call(e,r)&&(n[i]=t(r,e[r]),i+=1);return n}var o=Object.prototype.hasOwnProperty;t.exports=r},{}],3:[function(e,t,n){function r(e,t,n){t||(t=0),"undefined"==typeof n&&(n=e?e.length:0);for(var r=-1,o=n-t||0,i=Array(o<0?0:o);++r<o;)i[r]=e[t+r];return i}t.exports=r},{}],4:[function(e,t,n){t.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(e,t,n){function r(){}function o(e){function t(e){return e&&e instanceof r?e:e?c(e,u,i):i()}function n(n,r,o,i){if(!d.aborted||i){e&&e(n,r,o);for(var a=t(o),u=m(n),c=u.length,f=0;f<c;f++)u[f].apply(a,r);var p=s[y[n]];return p&&p.push([b,n,r,a]),a}}function l(e,t){v[e]=m(e).concat(t)}function m(e){return v[e]||[]}function w(e){return p[e]=p[e]||o(n)}function g(e,t){f(e,function(e,n){t=t||"feature",y[n]=t,t in s||(s[t]=[])})}var v={},y={},b={on:l,emit:n,get:w,listeners:m,context:t,buffer:g,abort:a,aborted:!1};return b}function i(){return new r}function a(){(s.api||s.feature)&&(d.aborted=!0,s=d.backlog={})}var u="nr@context",c=e("gos"),f=e(2),s={},p={},d=t.exports=o();d.backlog=s},{}],gos:[function(e,t,n){function r(e,t,n){if(o.call(e,t))return e[t];var r=n();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(e,t,{value:r,writable:!0,enumerable:!1}),r}catch(i){}return e[t]=r,r}var o=Object.prototype.hasOwnProperty;t.exports=r},{}],handle:[function(e,t,n){function r(e,t,n,r){o.buffer([e],r),o.emit(e,t,n)}var o=e("ee").get("handle");t.exports=r,r.ee=o},{}],id:[function(e,t,n){function r(e){var t=typeof e;return!e||"object"!==t&&"function"!==t?-1:e===window?0:a(e,i,function(){return o++})}var o=1,i="nr@id",a=e("gos");t.exports=r},{}],loader:[function(e,t,n){function r(){if(!x++){var e=h.info=NREUM.info,t=d.getElementsByTagName("script")[0];if(setTimeout(s.abort,3e4),!(e&&e.licenseKey&&e.applicationID&&t))return s.abort();f(y,function(t,n){e[t]||(e[t]=n)}),c("mark",["onload",a()+h.offset],null,"api");var n=d.createElement("script");n.src="https://"+e.agent,t.parentNode.insertBefore(n,t)}}function o(){"complete"===d.readyState&&i()}function i(){c("mark",["domContent",a()+h.offset],null,"api")}function a(){return E.exists&&performance.now?Math.round(performance.now()):(u=Math.max((new Date).getTime(),u))-h.offset}var u=(new Date).getTime(),c=e("handle"),f=e(2),s=e("ee"),p=window,d=p.document,l="addEventListener",m="attachEvent",w=p.XMLHttpRequest,g=w&&w.prototype;NREUM.o={ST:setTimeout,SI:p.setImmediate,CT:clearTimeout,XHR:w,REQ:p.Request,EV:p.Event,PR:p.Promise,MO:p.MutationObserver};var v=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1071.min.js"},b=w&&g&&g[l]&&!/CriOS/.test(navigator.userAgent),h=t.exports={offset:u,now:a,origin:v,features:{},xhrWrappable:b};e(1),d[l]?(d[l]("DOMContentLoaded",i,!1),p[l]("load",r,!1)):(d[m]("onreadystatechange",o),p[m]("onload",r)),c("mark",["firstbyte",u],null,"api");var x=0,E=e(4)},{}]},{},["loader"]);</script>
<!--[if lte IE 9]>
    <script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>
  <![endif]-->
</head>
<body class="application pages show">

<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-PRPXBQ6"
  height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>

<div id="outer-wrapper">
<div id="inner-wrapper">
<div id="messaging-wrapper" data-load="https://www.adafruit.com/api/multi_message.php"></div>
<header id="adafruit-header">
<div id="small-header-content" class="container visible-xs">
<a id="small-header-menu-button" class="menu-link" href="#small-header-nav">
<i class="fa fa-bars"> </i>
</a>
<div class="small-header-logo">
<a href="https://www.adafruit.com">
<img id="small-logo" height="50" width="50" alt="Adafruit Logo" title="Adafruit Logo" src="/logos/adafruit_logo_small.png?-2390980490884142940" />
</a> </div>
<a class="small-header-cart" href="https://www.adafruit.com/shopping_cart">
<span class="small-cart-count">0</span>
<i class="fa fa-shopping-cart"></i>
</a> </div>
<nav id="small-header-nav" role="navigation" class="visible-xs">
<div class="block">
<ul>
<li>
<div id="small-search-wrapper">
<div id="small-search-inner-wrapper">
<form action="https://learn.adafruit.com/search" method="get">
<label for="mobile-search" style="display:none;">Search</label>
<input id="mobile-search" type="text" name="q" placeholder="Search Adafruit" />
<i class="fa fa-search"></i>
</form>
</div>
</div>
</li>
<li>
<a href="https://www.adafruit.com/categories">SHOP</a>
</li>
<li>
<a href="https://blog.adafruit.com">BLOG</a>
</li>
<li>
<a href="https://learn.adafruit.com">LEARN</a>
</li>
<li>
<a href="https://forums.adafruit.com">FORUMS</a>
</li>
<li>
<a href="https://www.youtube.com/adafruit">VIDEOS</a>
</li>
<li>
<a href="/users/sign_in">SIGN IN</a>
</li>
<li>
<a class="close-btn" id="small-nav-close-button" href="#top">CLOSE MENU</a>
</li>
</ul>
</div>
</nav>
<div id="header-content" class="container hidden-xs">
<div id="header-profile">
<a id="header-cart" href="https://www.adafruit.com/shopping_cart">
0 Items <i class="fa fa-shopping-cart"></i>
</a> <div id="account">
<a href="/users/sign_in">Sign In</a>
</div>
<div id="search-wrapper">
<form action="/search" method="get">
<label for="search" style="display:none;">Search</label>
<input id="search" type="text" name="q" autocomplete="off" data-page="" , data-app-id="W9DMM4OTH0" data-app-key="e613bcda3453b9ef887e2724362f9e57" data-app-index="learn_guides_production" data-app-uri="https://learn.adafruit.com" />
<i class="fa fa-search"></i>
<input type="submit" style="visibility: hidden; position: fixed;">
</form>
</div>
</div>
<div id="navigation">
<a href="https://www.adafruit.com">
<img id="logo" width="172" height="60" alt="Adafruit Logo" title="Adafruit Logo" src="/logos/logo_2x.png?-2390980490884142940" />
</a> <nav class="hover-menu">
<ul>
<li id="nav-shop" data-load="https://www.adafruit.com/api/flyouts/shop.html"><a href="https://www.adafruit.com">SHOP</a>
</li>
<li id="nav-blog" data-load="https://blog.adafruit.com/adafruit-blog-flyouts"><a href="https://blog.adafruit.com">BLOG</a>
</li>
<li id="nav-learn" data-load="https://learn.adafruit.com/api/hover-menu/flyouts/learn.html"><a href="https://learn.adafruit.com">LEARN</a>
</li>
<li id="nav-forums"><a href="https://forums.adafruit.com">FORUMS</a>
</li>
<li id="nav-forums"><a href="https://www.youtube.com/adafruit">VIDEOS</a>
</li>
<li class="visible-lg"><a href="https://www.adabox.com">ADABOX</a></li>
</ul>
</nav>
</div>
</div>
</header>
<div id="main-content">
<div id="page-wrapper">
<div id="content-wrapper" class="container" data-page-id="3077" data-guide-id="480">
<div class="row">
<div class="sidebar-left-wrapper hidden-phone hidden-tablet col-lg-two-and-half col-md-3 col-sm-4 col-xs-12">
<div class="sidebar-left-content" data-clampedwidth=".sidebar-left-wrapper">
<nav class="sidebar-left">
<div class="title-bar">
<img src='https://cdn-learn.adafruit.com/guides/images/000/000/480/medium800/DSC00396.jpg?1448301599' class='img img-responsive' />
<div class="title">
<h1><a href="/raspberry-pi-face-recognition-treasure-box/overview">Raspberry Pi Face Recognition Treasure Box</a></h1>
<span class="tagline"><a href="/raspberry-pi-face-recognition-treasure-box/overview">Create a box that only opens when the right person looks at it!</a></span>
 </div>
</div>
<ul class="page-parent nav">
<li class='parent active'>
<a href="#overview" class="sidebar-parent">Overview</a>
<span class="page-draft-status">
</span>
</li>
<li class='parent '>
<a href="#hardware" class="sidebar-parent">Hardware</a>
<span class="page-draft-status">
</span>
</li>
<li class='parent '>
<a href="#software" class="sidebar-parent">Software</a>
<span class="page-draft-status">
</span>
</li>
<li class='parent '>
<a href="#training-1" class="sidebar-parent">Training</a>
<span class="page-draft-status">
</span>
</li>
<li class='parent '>
<a href="#configuration" class="sidebar-parent">Configuration</a>
<span class="page-draft-status">
</span>
</li>
<li class='parent '>
<a href="#usage" class="sidebar-parent">Usage</a>
<span class="page-draft-status">
</span>
</li>
<li class='parent '>
<a href="#future-work" class="sidebar-parent">Future Work</a>
<span class="page-draft-status">
</span>
</li>
<li class="single-page-spacer"></li>
<li class="single-page-link"><a href="/raspberry-pi-face-recognition-treasure-box">Multiple Pages</a></li>
<li><a href="https://cdn-learn.adafruit.com/downloads/pdf/raspberry-pi-face-recognition-treasure-box.pdf">Download PDF</a></li>
</ul>
</nav>
<header class="sidebar-meta hidden-xs">
<h4>Contributors</h4>
<div><a href="/users/tdicola">Tony DiCola</a></div>
</header>
<header class="sidebar-meta hidden-xs">
<a class="feedback-link" title="Feedback? Corrections?" rel="nofollow" data-remote="true" data-method="get" href="/pages/3077/settings_modal">
Feedback? Corrections?
</a> </header>
</div>
</div>
<article class="col-lg-7 col-md-6 col-sm-8 col-xs-12">
<div id="categories">
<span class="category ">
<a href="/category/projects">PROJECTS</a>
</span>
<span class="category child-category">
<a href="/category/sensors">SENSORS</a>
<span class="category-link-spacer">/</span>
<a href="/category/camera">CAMERA</a>
</span>
<span class="category child-category">
<a href="/category/raspberry-pi">RASPBERRY PI</a>
<span class="category-link-spacer">/</span>
<a href="/category/pi-b-plus-2-3">PI A+, B+, 2, 3</a>
</span>
<span id="guide-favorite">
<a class="favorites-link category right red" title="Favorite this guide?" data-toggle="tooltip" data-placement="left" data-remote="true" rel="nofollow" data-method="post" href="/guides/480/favorites.js">
<i class="fa fa-heart-o"></i>
</a></span>
</div>
<div class="content">
<div class="page-title-wrapper">
<h1 class="headline">
<span id="overview">Overview</span>
</h1>
<div class="author">by
<a href="/users/tdicola">
<span class="name">Tony DiCola</span>
</a> </div>
</div>
<div class="page-content all-page-view-content">
<div class="build-embed">
<div class='build-video'><iframe width="480" height="270" src="https://www.youtube.com/embed/CTP9rpgabYI?feature=oembed" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></div>
</div>
<div class="row-fluid build-text">
Face recognition is an exciting field of computer vision with many possible applications to hardware and devices. Using embedded platforms like the Raspberry Pi and open source computer vision libraries like <a href="http://opencv.org/">OpenCV</a>, you can now add face recognition to your own maker projects! In this project I'll show you how to build a treasure box which unlocks itself using face recognition running on a Raspberry Pi.<br>
</div>
<div class="row-fluid build-image">
<a href="/assets/13672">
<img class="13672-asset img-responsive" srcset="https://cdn-learn.adafruit.com/assets/assets/000/013/672/medium260/raspberry_pi_DSC00396.jpg?1390291779 260w,
               https://cdn-learn.adafruit.com/assets/assets/000/013/672/medium640/raspberry_pi_DSC00396.jpg?1390291779 640w,
               https://cdn-learn.adafruit.com/assets/assets/000/013/672/medium800/raspberry_pi_DSC00396.jpg?1390291779 800w,
               https://cdn-learn.adafruit.com/assets/assets/000/013/672/large1024/raspberry_pi_DSC00396.jpg?1390291779 1024w" sizes="(max-width: 768px) 100vw, (max-width: 1024px) 65vw, (max-width: 1365px) 47vw, 750px" src="https://cdn-learn.adafruit.com/assets/assets/000/013/672/medium800/raspberry_pi_DSC00396.jpg?1390291779" alt="raspberry_pi_DSC00396.jpg" />
<span class="image-expand"><i class="fa fa-search-plus"></i></span>
</a> </div>
<div class="row-fluid build-text">
Before you get started with this project, it will help to familiarize yourself with a few things:<br><ul>
<li>If you haven't setup or used a Raspberry Pi, go through the tutorials on <a href="http://learn.adafruit.com/category/learn-raspberry-pi">learning the Raspberry Pi</a> like <a href="http://learn.adafruit.com/adafruit-raspberry-pi-lesson-1-preparing-and-sd-card-for-your-raspberry-pi">preparing an SD card</a>, <a href="http://learn.adafruit.com/adafruits-raspberry-pi-lesson-3-network-setup">network setup</a>, and <a href="http://learn.adafruit.com/adafruits-raspberry-pi-lesson-6-using-ssh">using SSH</a> before attempting this project. Also take a look at the <a href="http://learn.adafruit.com/adafruits-raspberry-pi-lesson-8-using-a-servo-motor">lesson on using a servo</a> for more background on how servos work.<br>
</li>
<li>Skim the <a href="http://docs.opencv.org/trunk/modules/contrib/doc/facerec/facerec_tutorial.html">OpenCV tutorial on face recognition</a> for an idea of how face recognition algorithms work. Don't worry, you don't need to fully understand the math or code to build and learn from this project.</li>
</ul>Continue on to learn about the hardware needed to build this project.<br>
</div>
</div>
<div class="page-title-wrapper">
<h1 class="headline">
<span id="hardware">Hardware</span>
</h1>
<div class="author">by
<a href="/users/tdicola">
<span class="name">Tony DiCola</span>
</a> </div>
</div>
<div class="page-content all-page-view-content">
<div class="row-fluid build-text">
You will need the following parts for this project:<br><ul>
<li>Raspberry Pi, either <a href="http://www.adafruit.com/products/1344">model A</a> or <a href="http://www.adafruit.com/products/998">model B</a> will work, running the <a title="Link: http://www.raspbian.org/" href="http://www.raspbian.org/">Raspbian</a> operating system.</li>
<ul><li>Your Pi will need access to the internet to setup the software, so make sure you have either a wired or <a href="http://www.adafruit.com/products/814">wireless</a> network connection setup with your Pi.</li></ul>
<li>
<a href="http://www.adafruit.com/products/1367">Raspberry Pi camera</a>.</li>
<ul><li>Depending on where your camera and Raspberry Pi can be placed inside your box, you might need a <a href="http://www.adafruit.com/products/1648">longer</a> or <a href="http://www.adafruit.com/products/1645">shorter</a> camera cable.</li></ul>
<li>Small box that can fit the Raspberry Pi and locking mechanism inside. I found an inexpensive plain wooden box at a craft store, and finished it with wood stain and polyurethane.</li>
<ul><li>Look for a box that has hinges which are screwed in from the outside of the box. Although not terribly secure, it will allow you to disassemble and open the box in case the locking mechanism fails to open.</li></ul>
<li>Small servo or lock solenoid for the locking mechanism, depending on how your box can be latched shut.</li>
<ul>
<li>A <a title="Link: http://www.adafruit.com/products/169" href="http://www.adafruit.com/products/169">servo</a> that rotates a latch can work with most boxes that open from the top or side.</li>
<li>A <a href="http://www.adafruit.com/products/1512">lock solenoid</a> can work with boxes that have a door or drawer. See <a href="http://learn.adafruit.com/secret-knock-activated-drawer-lock">this locking drawer project</a> for information on using a lock solenoid. <b>Note:</b> the software for this project is written to use a servo as the locking mechanism, so if you use a lock solenoid you will need to modify the software to actuate the lock with the solenoid instead of the servo.</li>
</ul>
<ul></ul>
<li>
<a href="http://www.adafruit.com/products/1505">Momentary push button</a> that can mount to the box. Depending on how thick your box is, you might need a smaller or larger push button.</li>
<li>10 kilo-ohm 1/4 watt resistor to use as a pull-up resistor with the push button.</li>
<li>
<a href="http://www.adafruit.com/products/501">Power supply for the Raspberry Pi</a> and servo or solenoid. For powering a micro servo, a <a href="http://www.adafruit.com/products/830">4x AA battery pack</a> is a simple option.</li>
<li>Wood, wood glue, and fasteners for building a latch mechanism and frame to support the Pi inside the box. The exact material will depend on your box, but you can see further below how I used 1/4" dowel and thin bass wood to build the frame and latching mechanism for my box.</li>
<li>
<a href="http://www.adafruit.com/products/1311">Hookup wires</a> to connect the switch, servo, and servo power supply. <a href="http://www.adafruit.com/products/824">Female hookup wires</a> work well for connecting directly to the Raspberry Pi GPIO pins, or you could use the <a href="http://www.adafruit.com/products/914">Pi cobbler</a> with a <a href="http://www.adafruit.com/products/64">small breadboard</a>.</li>
</ul>
</div>
<div class="row-fluid build-alert">
<div class="alert">
<i class='fa fa-exclamation-circle'></i>
Note: This project is not meant to be a highly secure container. Face recognition is not perfect and can easily be circumvented with a photograph. Don't store valuables in the box!
</div>
</div>
<div class="row-fluid build-text">
<h2>
<a href="#assembly" class="anchor-link"><span class="fa fa-link"></span></a><span id="assembly" class="anchor-link-target"></span>Assembly</h2>The box you use for your project will dictate exactly how the Raspberry Pi, servo, and latching mechanism need to be mounted. Read the notes below for tips on how to construct your hardware, based on how I built mine:
</div>
<table class="build-table">
<tr class="build-row">
<td class="side-images">
<a href="#step-4" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-4" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13728">
<img class='13728-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/728/medium640/raspberry_pi_DSC00374.jpg?1390376164' alt='raspberry_pi_DSC00374.jpg' />
</a></li>
<li class="small-side">
<a class="medium-side-image-link" href="/assets/13728">
<img class='13728-asset small-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/728/thumb160/raspberry_pi_DSC00374.jpg?1390376164' alt='raspberry_pi_DSC00374.jpg' />
</a> </li>
<li class="small-side">
<a class="medium-side-image-link" href="/assets/13732">
<img class='13732-asset small-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/732/thumb160/raspberry_pi_DSC00376.jpg?1390376417' alt='raspberry_pi_DSC00376.jpg' />
</a> </li>
</ul>
</td>
<td class="side-text"><div class="text">Use a box which can fit the Raspberry Pi, servo, and latching mechanism.<br><br>Drill a hole in the top or side for the Raspberry Pi camera. I found a 7/16" drill bit was enough for the camera to comfortably fit. Be careful when drilling large holes--work up from smaller bits so you don't crack the box. If you do damage the box, you can generally use wood filler to hide mistakes.<br><br>If they aren't mounted there already, consider moving the hinges to be mounted from the outside of the box. This will allow you to disassemble the box in case the hardware fails in a locked position.<br><br>Drill a hole in the box to mount the push button. You can see I mounted mine on the back of the box where it can be reached while a user looks into the camera on the top.<br><br>Drill another hole to allow power cables to come into the box for both the Raspberry Pi and servo. I found a 1/2" hole was enough to fit a micro USB cable through for powering the Pi. To the left, you can see the hole I drilled in my box next to the push button.</div></td>
</tr>
<tr class="build-row">
<td class="side-images">
<a href="#step-5" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-5" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13733">
<img class='13733-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/733/medium640/raspberry_pi_DSC00397.jpg?1390376489' alt='raspberry_pi_DSC00397.jpg' />
</a></li>
<li class="small-side">
<a class="medium-side-image-link" href="/assets/13733">
<img class='13733-asset small-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/733/thumb160/raspberry_pi_DSC00397.jpg?1390376489' alt='raspberry_pi_DSC00397.jpg' />
</a> </li>
<li class="small-side">
<a class="medium-side-image-link" href="/assets/13734">
<img class='13734-asset small-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/734/thumb160/raspberry_pi_DSC00384.jpg?1390376555' alt='raspberry_pi_DSC00384.jpg' />
</a> </li>
<li class="small-side">
<a class="medium-side-image-link" href="/assets/13735">
<img class='13735-asset small-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/735/thumb160/raspberry_pi_DSC00377.jpg?1390376601' alt='raspberry_pi_DSC00377.jpg' />
</a> </li>
<li class="small-side">
<a class="medium-side-image-link" href="/assets/13736">
<img class='13736-asset small-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/736/thumb160/raspberry_pi_DSC00381.jpg?1390376654' alt='raspberry_pi_DSC00381.jpg' />
</a> </li>
</ul>
</td>
<td class="side-text"><div class="text">For the latching mechanism, mount a small dowel perpendicular to the side of the box. Attach a right angle of wood to a servo horn so it can act as a latch that swings down to catch the dowel, locking the box. See the pictures to the left to see the latch mechanism and dowel I built in my box.<br><br>If possible, mount the Raspberry Pi in the top of the box or near the hole for the camera. You can see how I mounted my Pi to a small board along with the locking servo, and then attached that board to dowels glued in to form a frame in the box top.<br><br> A few screws and a smaller board can act as a clamp to hold the servo in place.<br></div></td>
</tr>
</table>
<div class="row-fluid build-text">
<h2>
<a href="#wiring" class="anchor-link"><span class="fa fa-link"></span></a><span id="wiring" class="anchor-link-target"></span>Wiring</h2>The electronics in this project are fairly simple and involve connecting a servo and push button to the Rasperry Pi. If you have never used these devices with a Raspberry Pi, read the following tutorials for a good overview of their usage:<br><ul>
<li><a href="http://learn.adafruit.com/adafruits-raspberry-pi-lesson-4-gpio-setup">Raspberry Pi Lesson 4: GPIO Setup</a></li>
<li><a href="http://learn.adafruit.com/adafruits-raspberry-pi-lesson-8-using-a-servo-motor">Raspberry Pi Lesson 8: Using a Servo Motor</a></li>
<li><a href="http://learn.adafruit.com/playing-sounds-and-using-buttons-with-raspberry-pi/bread-board-setup-for-input-buttons">Bread Board Setup for Input Buttons</a></li>
</ul>For the servo, connect the signal line to GPIO 18 of the Raspberry Pi. To power the servo I connected a 4x AA battery pack as a power source--connecting the servo to the Pi's 5 volt output could cause problems from noise or excessive current drawn by the servo. <br><br>The push button is attached to GPIO 25 of the Raspberry Pi, with a 10 kilo-ohm pull-up resistor to 3.3 volt power from the Pi.<br><br>See the diagram below for how to wire the push button and servo to the Raspberry Pi.
</div>
<div class="row-fluid build-image">
<a href="/assets/13739">
<img class="13739-asset img-responsive" srcset="https://cdn-learn.adafruit.com/assets/assets/000/013/739/medium260/raspberry_pi_pi-facebox_bb.png?1390378813 260w,
               https://cdn-learn.adafruit.com/assets/assets/000/013/739/medium640/raspberry_pi_pi-facebox_bb.png?1390378813 640w,
               https://cdn-learn.adafruit.com/assets/assets/000/013/739/medium800/raspberry_pi_pi-facebox_bb.png?1390378813 800w,
               https://cdn-learn.adafruit.com/assets/assets/000/013/739/large1024/raspberry_pi_pi-facebox_bb.png?1390378813 1024w" sizes="(max-width: 768px) 100vw, (max-width: 1024px) 65vw, (max-width: 1365px) 47vw, 750px" src="https://cdn-learn.adafruit.com/assets/assets/000/013/739/medium800/raspberry_pi_pi-facebox_bb.png?1390378813" alt="raspberry_pi_pi-facebox_bb.png" />
<span class="image-expand"><i class="fa fa-search-plus"></i></span>
</a> </div>
<div class="row-fluid build-text">
Continue on to learn about how the dependencies and software set up for the project.
</div>
</div>
<div class="page-title-wrapper">
<h1 class="headline">
<span id="software">Software</span>
</h1>
<div class="author">by
<a href="/users/tdicola">
<span class="name">Tony DiCola</span>
</a> </div>
</div>
<div class="page-content all-page-view-content">
<div class="row-fluid build-alert alert-danger">
<div class="alert">
<i class='fa fa-exclamation-circle'></i>
Note this project was created in 2013 and the Raspberry Pi operating system has since been updated to not be compatible with the RPIO library mentioned below. Use an older version of Raspbian like a wheezy release from 2013 from: <a href="http://downloads.raspberrypi.org/raspbian/images/">http://downloads.raspberrypi.org/raspbian/images/</a>
</div>
</div>
<div class="row-fluid build-text">
<h2>
<a href="#opencv-installation" class="anchor-link"><span class="fa fa-link"></span></a><span id="opencv-installation" class="anchor-link-target"></span>OpenCV Installation</h2>
<p>This project depends on the <a href="http://opencv.org/">OpenCV</a> computer vision library to perform the face detection and recognition. Unfortunately the current binary version of OpenCV available to install in the Raspbian operating system through apt-get (version 2.3.x) is too old to contain the <a href="http://docs.opencv.org/modules/contrib/doc/facerec/facerec_tutorial.html">face recognition algorithms</a> used by this project. However you can download, compile, and install a later version of OpenCV to access the face recognition algorithms.<br><br><strong>Note: </strong> Compiling OpenCV on the Raspberry Pi will take about 5 hours of mostly unattended time. Make sure you have some time to start the process before proceeding.<br><br>First you will need to install OpenCV dependencies before you can compile the code. Connect to your Raspberry Pi in a terminal session and execute the following command:<br><br>sudo apt-get update<br>sudo apt-get install build-essential cmake pkg-config python-dev libgtk2.0-dev libgtk2.0 zlib1g-dev libpng-dev libjpeg-dev libtiff-dev libjasper-dev libavcodec-dev swig unzip<br><br>Answer yes to any questions about proceeding and wait for the libraries and dependencies to be installed. You can ignore messages about packages which are already installed.<br><br>Next you should download and unpack the OpenCV source code by executing the following commands:<br><br>wget http://downloads.sourceforge.net/project/opencvlibrary/opencv-unix/2.4.9/opencv-2.4.9.zip<br>unzip opencv-2.4.9.zip<br><br>Note that this project was written using OpenCV 2.4.7, although any 2.4.x version of OpenCV should have the necessary face recognition algorithms.<br><br>Now change to the directory with the OpenCV source and execute the following cmake command to build the makefile for the project. Note that some of the parameters passed in to the cmake command will disable compiling performance tests and GPU accelerated algorithms in OpenCV. I found removing these from the OpenCV build was necessary to help reduce the compilation time, and successfully compile the project with the low memory available to the Raspberry Pi.<br><br>cd opencv-2.4.9<br>cmake -DCMAKE_BUILD_TYPE=RELEASE -DCMAKE_INSTALL_PREFIX=/usr/local -DBUILD_PERF_TESTS=OFF -DBUILD_opencv_gpu=OFF -DBUILD_opencv_ocl=OFF<br><br>After this command executes you should see details about the build environment and finally a '-- Build files have been written to: ...' message. You might see a warning that the source directory is the same as the binary directory--this warning can be ignored (most cmake projects build inside a subdirectory of the source, but for some reason I couldn't get this to work with OpenCV and built it inside the source directory instead). If you see any other error or warning, make sure the dependencies above were installed and try executing the cmake command again.<br><br>Next, compile the project by executing:<br><br>make<br><br>This process will take a significant amount of time (about 5 hours), but you can leave it unattended as the code compiles.<br><br>Finally, once compilation is complete you can install the compiled OpenCV libraries by executing:<br><br>sudo make install<br><br>After this step the latest version of OpenCV should be installed on your Raspberry Pi.<br><br></p>
<h2>
<a href="#python-dependencies" class="anchor-link"><span class="fa fa-link"></span></a><span id="python-dependencies" class="anchor-link-target"></span>Python Dependencies</h2>
<p>The code for this project is written in python and has a few dependencies that must be installed. Once connected to your Raspberry Pi in a terminal session, execute the following commands:<br><br>sudo apt-get install python-pip<br>sudo apt-get install python-dev<br>sudo pip install picamera<br>sudo pip install rpio<br><br>You can ignore any messages about packages which are already installed or up to date. These commands will install the <a href="http://picamera.readthedocs.org/en/release-1.0/">picamera library</a> for access to the Raspberry Pi camera, and the <a href="http://pythonhosted.org/RPIO/">RPIO library</a> for access to the Pi GPIO pins and PWM support (for better servo control with the Pi).<br><br></p>
<h2>
<a href="#software-install" class="anchor-link"><span class="fa fa-link"></span></a><span id="software-install" class="anchor-link-target"></span>Software Install</h2>
<p>After OpenCV and the python dependencies have been installed, download the software for this project from the link below:<br><br></p>
</div>
<div id="element-2278761" class="button-element" data-github-release="">
<a href="https://github.com/tdicola/pi-facerec-box/archive/master.zip" class="btn btn-large btn-block btn-primary" target="_self" type="button">Download Code</a>
</div>
<div class="row-fluid build-text">
Copy the archive to your Raspberry Pi and extract it to a folder.<br><br>Continue on to learn about training the face recognition algorithm to recognize your face.
</div>
</div>
<div class="page-title-wrapper">
<h1 class="headline">
<span id="training-1">Training</span>
</h1>
<div class="author">by
<a href="/users/tdicola">
<span class="name">Tony DiCola</span>
</a> </div>
</div>
<div class="page-content all-page-view-content">
<div class="row-fluid build-text">
<span>
This project uses the <a href="http://docs.opencv.org/trunk/modules/contrib/doc/facerec/facerec_tutorial.html">eigenfaces algorithm in OpenCV</a> to perform face recognition. To use this algorithm you'll need to create a set of training data with pictures of faces that are and are not allowed to open the box.<br></span>
<br>Included in the project is a large set of face images that are tuned for training with the face recognition algorithm. This is the <a href="http://www.cl.cam.ac.uk/research/dtg/attarchive/facedatabase.html">database of faces</a> published by research AT&amp;T Laboratories Cambridge in the mid 90's. These faces make up the set of negative images which represent faces that are not allowed to open the box. You can see these images in the <b>training/negative</b> subdirectory of the project.<br><br>To generate images of the person who will be allowed to open the box, or positive training images, you can use the included <b>capture-positives.py</b> script. This script will take pictures with the box hardware and write them to the <b>training/positive</b> sub-directory (which will be created by the script if it does not exist).<br><br>With the box hardware assembled and powered up (servo power is not necessary for this step), connect to the Raspberry Pi in a terminal session and navigate to the directory with the project software. Execute the following command to run the capture positive script:<br><br><span class="editor-monospace">sudo python capture-positives.py</span><br><br>After waiting a few moments for the script to load, you should see the following instructions:<br><br><span class="editor-monospace">Capturing positive training images.<br></span><span class="editor-monospace">Press button or type c (and press enter) to capture an image.<br></span><span class="editor-monospace">Press Ctrl-C to quit.<br></span><br>The script is now ready to capture images for training. If you see an error message, make sure OpenCV and the software dependencies from the <a href="http://learn.adafruit.com/raspberry-pi-face-recognition-treasure-box/software">previous step</a> are installed and try again.<br><br>Point the box's camera at your face and press the button on the box (or send the letter 'c' in the terminal session) to take a picture. If the script detects a single face, it will crop and save the image in the positive training images sub-directory. If the script can't detect a face or detects multiple faces, an error message will be displayed.<br><br>If see error messages about not detecting a single face, you can examine the full picture that was captured by the camera to understand if it's picking up your face (or if other faces might be in view--be careful, even photos or posters with faces behind you can be detected!). Open the file <b>capture.pgm</b> (located in the directory with the scripts) in an image editor to see the last image that was captured. It's easiest to use a tool like <a href="http://cyberduck.io/" title="Link: http://cyberduck.io/">Cyberduck</a> to view the files on your Raspberry Pi over SFTP (SSH file transfer protocol).<br><br>Using the capture-positives.py script, capture some pictures of the face that is allowed to open the box. Try to take pictures of the face with different expressions, under different lighting conditions, and at different angles. You can see the images I captured for my positive training data below:
</div>
<table class="build-table">
<tr class="build-row">
<td class="side-images">
<a href="#step-2" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-2" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13697">
<img class='13697-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/697/medium640/raspberry_pi_training_images.jpg?1390343498' alt='raspberry_pi_training_images.jpg' />
</a></li>
</ul>
</td>
<td class="side-text"><div class="text">Training images I captured for my face. Try to get pictures with different expressions, in different light, etc. to build a better face recognition model.</div></td>
</tr>
</table>
<div class="row-fluid build-text">
Once you've captured a number of positive training images, you can run the <b>train.py</b> script to perform the training. If it's still running, exit the <b>capture-positives.py</b> script by pressing Ctrl-C in the terminal session. Run the following python script to train the face recognition model:<br><br><span class="editor-monospace">python train.py</span><br><br>Note that this command does not need to be run as root with sudo because none of the Pi GPIO/hardware is accessed.<br><br>You should see a message that the training images were loaded, and the text '<span class="editor-monospace">Training model...</span>' to indicate the training calculations are being performed. Training the face recognition model on the Pi will take about 10 minutes.<br><br>Once the training is complete you should see the message '<span class="editor-monospace">Training data saved to training.xml</span>'. The training data is now stored in the file <b>training.xml</b>, which will be loaded by the box software to configure the face recognition model.<br><br>If you're curious you can examine images that are output by the training to visualize the eigenfaces of the model. Open the <b>mean.png</b>, <b>positive_eigenface.png</b>, and <b>negative_eigenface.png</b> files in an image viewer. You don't need to do anything with these images, but can learn more about their meaning from the <a href="http://docs.opencv.org/modules/contrib/doc/facerec/facerec_tutorial.html#eigenfaces">OpenCV website</a>, <a href="http://en.wikipedia.org/wiki/Eigenface">Wikipedia</a>, or the <a href="http://www.face-rec.org/algorithms/PCA/jcn.pdf">original research paper on eigenfaces</a>.<br><br>
</div>
<table class="build-table">
<tr class="build-row">
<td class="side-images">
<a href="#step-4" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-4" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13698">
<img class='13698-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/698/medium640/raspberry_pi_eigenfaces.jpg?1390343557' alt='raspberry_pi_eigenfaces.jpg' />
</a></li>
</ul>
</td>
<td class="side-text"><div class="text">Eigenfaces generated from my training data. <br><br>The positive eigenface is a summary of the features that differentiate my face from the average or mean face. This face will be allowed to unlock the box.<br><br>The negative eigenface represents all the other faces in the training set. This face will not be allowed to unlock the box.</div></td>
</tr>
</table>
<div class="row-fluid build-text">
With the <b>training.xml</b> file generated, you're ready to move on to configure the servo latch and software for the project.
</div>
</div>
<div class="page-title-wrapper">
<h1 class="headline">
<span id="configuration">Configuration</span>
</h1>
<div class="author">by
<a href="/users/tdicola">
<span class="name">Tony DiCola</span>
</a> </div>
</div>
<div class="page-content all-page-view-content">
 <div class="row-fluid build-text">
<h2>
<a href="#servo-configuration" class="anchor-link"><span class="fa fa-link"></span></a><span id="servo-configuration" class="anchor-link-target"></span>Servo Configuration</h2>In this step you'll determine the pulse width values for the locked and unlocked servo positions of the box. Make sure the hardware is assembled, the software dependencies are installed, and power is applied to both the Raspberry Pi and servo before you continue. Connect to the Raspberry Pi in a terminal session and type the following to run an interactive python shell as root:<br><br><span class="editor-monospace">sudo python</span><br><br>At the python shell type in the following to load the RPIO library and its servo control class (note you don't need to type the &gt;&gt;&gt;, it's just a reference for what you should see):<br><br><span class="editor-monospace">&gt;&gt;&gt; from RPIO import PWM</span><br><span class="editor-monospace">&gt;&gt;&gt; servo = PWM.Servo()</span><br><br>Now you can call the set_servo function to send pulse width values to the servo which will move it to different positions. The pulse width value you send can range from 1000 to 2000 microseconds, with a value of 1500 being the center position of the servo. If you're curious, you can find more information on servos <a href="http://learn.adafruit.com/adafruits-raspberry-pi-lesson-8-using-a-servo-motor">in this tutorial</a>.<br><br>Make sure the box is open so you can see the servo and it's free to move, then execute this command to move the servo to the center position (pulse width of 1500 microseconds):<br><br><span class="editor-monospace">&gt;&gt;&gt; servo.set_servo(18, 1500)</span><br><br>Note that if your servo is connected to a different GPIO port of the Raspberry Pi, change the first parameter from 18 to the appropriate value.<br><br>Try sending different pulse width values between 1000 and 2000 to find the values which move the latch to the locked and unlocked position. Don't forget you can adjust the position of the servo horn and latch on the servo if necessary. You can see the values I found for my hardware below:<br>
</div>
<table class="build-table">
<tr class="build-row">
<td class="side-images">
<a href="#step-2" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-2" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13674">
<img class='13674-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/674/medium640/raspberry_pi_DSC00392.jpg?1390334645' alt='raspberry_pi_DSC00392.jpg' />
</a></li>
</ul>
</td>
<td class="side-text"><div class="text">Latch in the unlocked position with a servo pulse width of 2000 micro seconds.</div></td>
</tr>
<tr class="build-row">
<td class="side-images">
<a href="#step-3" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-3" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13675">
<img class='13675-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/675/medium640/raspberry_pi_DSC00391.jpg?1390334757' alt='raspberry_pi_DSC00391.jpg' />
</a></li>
</ul>
</td>
<td class="side-text"><div class="text">Latch in the locked position with a servo pulse width of 1100 micro seconds.</div></td>
</tr>
</table>
<div class="row-fluid build-text">
Take note of the pulse width values you determined for the locked and unlocked position as they will be used later in the configuration. Execute the following command in the python shell to close it:<br><br><span><span class="editor-monospace">&gt;&gt;&gt; quit()</span><br><br><h2>
<a href="#software-configuration" class="anchor-link"><span class="fa fa-link"></span></a><span id="software-configuration" class="anchor-link-target"></span>Software Configuration</h2>In the directory with code for this project, open the file <b>config.py</b> in a text editor. This file defines the configuration for the project and might require a few changes for your hardware. Specifically you can adjust the following values:<br><ul>
<li>
<b>LOCK_SERVO_PIN </b>- this should be the GPIO number of the Raspberry Pi which is connected to the signal line of the lock servo. This project is built to use GPIO 18 by default.</li>
<li>
<b>LOCK_SERVO_UNLOCKED</b> - this should be the pulse width value (in microseconds) for the unlocked position of the latch. Use the value you determined in the previous step.</li>
<li>
<b>LOCK_SERVO_LOCKED</b> - this should be the pulse width value for the locked position of the latch.</li>
<li>
<b>BUTTON_PIN</b> - this should be the GPIO number which is connected to the push button on the box. This project is built to use GPIO 25 by default.</li>
</ul>The rest of the values in the configuration can be ignored. The only other value of interest is the <b>POSITIVE_THRESHOLD</b> configuration, which gives the boundary for how confident the face recognition has to be before it's considered a positive match. For now the default value of 2000 should suffice, but it can be adjusted later if the box has too many false positive or false negative recognitions.<br><br>Continue on to run the box software and finish the project.</span><span class="editor-monospace"><br></span>
</div>
</div>
<div class="page-title-wrapper">
<h1 class="headline">
<span id="usage">Usage</span>
</h1>
<div class="author">by
<a href="/users/tdicola">
<span class="name">Tony DiCola</span>
</a> </div>
</div>
<div class="page-content all-page-view-content">
<div class="row-fluid build-text">
To run the box software, make sure the hardware is assembled and the <a href="http://learn.adafruit.com/raspberry-pi-face-recognition-treasure-box/training-1">training</a> is complete. First you'll run the box with only power to the Raspberry Pi and not the lock servo--this will allow you to test the face recognition without locking yourself out of the box. Apply power to just the Raspberry Pi (and not the servo), then connect to the Pi in a terminal session, navigate to the folder with the software, and execute the following command:<br><br><span class="editor-monospace">sudo python box.py</span><br><br>You should see the box software load and the message '<span class="editor-monospace">Loading training data...</span>' appear. It should take a few minutes for the training data to load and the following message to appear:<br><br><span class="editor-monospace">Running box...</span>
<br><span class="editor-monospace">Press button to lock (if unlocked), or unlock if the correct face is detected.</span>
<br><span class="editor-monospace">Press Ctrl-C to quit.</span>
<br><br>The box will lock itself (however because no power is applied to the servo, the lock latch should not move) and be ready to try unlocking with face recognition. Aim the box camera at your face, like you did when training the face recognition model, and press the button on the box. You should see a message that the button was pressed, and after a moment if the face is recognized you will see a message like:<br><br><span class="editor-monospace">Predicted POSITIVE face with confidence 1321.35253959 (lower is more confident).</span>
<span class="editor-monospace">Recognized face!</span>
<br><br>If the face is not recognized you will see a message like:<br><br><span class="editor-monospace">Predicted NEGATIVE face with confidence 3987.76625152 (lower is more confident).</span>
<span>
<span class="editor-monospace">Did not recognize face!</span><br><br>If a single face couldn't be detected (because none is visible, or there are multiple faces detected) an error message will be displayed like with the training script.<br><br>When a face is found, you'll notice the prediction message includes how the face was recognized (i.e. matching either the positive or negative training data), and the confidence of the recognition. The confidence is a value like 1321.35 or 3987.77 above and represents the distance of the captured face from the predicted face--a lower distance value means the captured face is more similar to the predicted face.<br><br>To unlock the box, a captured face must be a positive prediction with a confidence value below the <b>POSITIVE_THRESHOLD</b> configuration value. By default the <b>POSITIVE_THRESHOLD</b> is 2000, so the positive prediction with confidence 1321.35 was considered a match and would have unlocked the box.<br><br>When the box is in an unlocked state, press the button to lock the box again. You do not need to have a face recognized to lock the box.<br><br>Play with unlocking and locking the box to see what prediction and confidence you get from your trained face recognition model. Ideally you want images of the positively trained face to be predicted as positive images with a low number for the confidence value. The eigenfaces recognition algorithm is sensitive to the lighting and orientation of your face, so try to have as similar conditions as when the positive training images were captured (or consider re-training your model to include more varied images).<br><br>You can see examples of how my training data predicted faces below (remember you can look at the <b>capture.pgm</b> image in the software directory after pressing the button to attempt a face recognition):</span><br>
</div>
<table class="build-table">
<tr class="build-row">
<td class="side-images">
<a href="#step-2" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-2" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13703">
<img class='13703-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/703/medium640/raspberry_pi_positive_capture.jpg?1390351605' alt='raspberry_pi_positive_capture.jpg' />
</a></li>
</ul>
</td>
<td class="side-text"><div class="text">This image unlocked my box because it was a match for the positive training images, and had a confidence of 1321.35 which was below the threshold of 2000.</div></td>
</tr>
<tr class="build-row">
<td class="side-images">
<a href="#step-3" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-3" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13704">
<img class='13704-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/704/medium640/raspberry_pi_negative_capture.jpg?1390351642' alt='raspberry_pi_negative_capture.jpg' />
</a></li>
</ul>
</td>
<td class="side-text"><div class="text">This image of a face from a magazine did not unlock my box because it was a match for the negative training data, with a confidence of 3987.77.</div></td>
</tr>
<tr class="build-row">
<td class="side-images">
<a href="#step-4" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-4" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13705">
<img class='13705-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/705/medium640/raspberry_pi_false_negative_capture.jpg?1390352556' alt='raspberry_pi_false_negative_capture.jpg' />
</a></li>
</ul>
</td>
<td class="side-text"><div class="text">This image unfortunately did not unlock my box. Although it was predicted as a positive match, the confidence was 2269.04 which was slightly higher than the positive match threshold. <br><br>If you get a lot of false negative predictions like this, it's a sign you need better training data or should adjust the <b>POSITIVE_THRESHOLD</b> configuration value up.</div></td>
</tr>
<tr class="build-row">
<td class="side-images">
<a href="#step-5" class='anchor-link'><span class='fa fa-link'></span></a>
<span id="step-5" class='anchor-link-target'></span>
<ul>
<li class="medium-side">
<a class="large-side-image-link" href="/assets/13707">
<img class='13707-asset medium-side-image img-responsive' src='https://cdn-learn.adafruit.com/assets/assets/000/013/707/medium640/raspberry_pi_false_positive_capture.jpg?1390353189' alt='raspberry_pi_false_positive_capture.jpg' />
</a></li>
</ul>
</td>
<td class="side-text"><div class="text">This image matched the positive training data, but the confidence value of 4407.85 was too far above the threshold to unlock the box. <br><br>If you get a lot of false positive responses like this it's also a sign that you need better training data. Remember face recognition is far from perfect--there's always a chance someone who looks like the positively trained images will match close enough to unlock the box!</div></td>
</tr>
</table>
<div class="row-fluid build-text">
Based on how the face recognition responds, you might consider training it again or adjust the <b>POSITIVE_THRESHOLD</b> configuration to a higher/lower value. <br><br>When you're happy with how the recognition is working, apply power to the servo and try locking and unlocking the box for real. Congratulations on building the face recognition treasure box!<br><br>If for some reason your box is locked and will not recognize a face to unlock itself, you can manually set the servo position to an unlocked value by following the steps in the <a href="http://learn.adafruit.com/raspberry-pi-face-recognition-treasure-box/configuration">servo configuration</a>. If you don't have access to the Raspberry Pi terminal or the servo isn't moving, unfortunately you'll need to disassemble your box (this is why it's a good idea to use a box with hinges on the outside!).<br>
</div>
</div>
<div class="page-title-wrapper">
<h1 class="headline">
<span id="future-work">Future Work</span>
</h1>
<div class="author">by
<a href="/users/tdicola">
<span class="name">Tony DiCola</span>
</a> </div>
</div>
<div class="page-content all-page-view-content">
<div class="row-fluid build-text">
This project is a great example of how to use the Raspberry Pi and Pi camera with OpenCV's computer vision algorithms. By compiling the latest version of OpenCV, you can get access to the latest and most interesting computer vision algorithms like face recognition. You can consider extending this project in other interesting ways, such as:<br><ul>
<li>Adding LED's to the box which flash when a face is detected and recognized. This feedback would help you train and use the box without having to connect to the Pi in a terminal session.</li>
<li>Make the main box.py script start up automatically when the Raspberry Pi powers on. Look at <a href="http://raspberrywebserver.com/serveradmin/run-a-script-on-start-up.html" title="Link: http://raspberrywebserver.com/serveradmin/run-a-script-on-start-up.html">this blog post</a> for more information on the various ways of automatically running a script at start up.</li>
<li>Investigate using other face recognition algorithms in OpenCV. See the <a href="http://docs.opencv.org/modules/contrib/doc/facerec/facerec_tutorial.html" title="Link: http://docs.opencv.org/modules/contrib/doc/facerec/facerec_tutorial.html">OpenCV tutorial on face recognition</a> for more information. Algorithms such as Fisherfaces might be more robust to varied lighting or other conditions.</li>
<li>Have the box send you an email with a picture of whoever is attempting to open it.</li>
<li>Add a microphone and look at adding <a href="http://raspberrypi.stackexchange.com/a/10392" title="Link: http://raspberrypi.stackexchange.com/a/10392">speech recognition</a> as another means of unlocking the box.</li>
</ul>Can you think of other ways to extend the project?<br>
</div>
</div>
</div>
</article>
<div class="col-lg-two-and-half col-md-3 hidden-sm hidden-xs">
<header class="sidebar-right">
<div class="sidebar-right-content">
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/1648">
<img src="https://cdn-shop.adafruit.com/640x480/1648-00.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">Flex Cable for Raspberry Pi Camera or Display - 300mm / 12&quot;</div>
<span class="product-price">$1.95</span>
<a id="1648-product" class="product-buy btn " data-pid="1648" data-qty="1" data-name="Flex Cable for Raspberry Pi Camera or Display - 300mm / 12&quot;" data-price="1.95" href="https://www.adafruit.com/product/1648">
Add to Cart
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/814">
<img src="https://cdn-shop.adafruit.com/640x480/814-07.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">Miniature WiFi (802.11b/g/n) Module: For Raspberry Pi and more</div>
<span class="product-price">$11.95</span>
<a id="814-product" class="product-buy btn " data-pid="814" data-qty="1" data-name="Miniature WiFi (802.11b/g/n) Module: For Raspberry Pi and more" data-price="11.95" href="https://www.adafruit.com/product/814">
Add to Cart
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/169">
<img src="https://cdn-shop.adafruit.com/640x480/169-06.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">Micro servo</div>
<span class="product-price">$5.95</span>
<a id="169-product" class="product-buy btn " data-pid="169" data-qty="1" data-name="Micro servo" data-price="5.95" href="https://www.adafruit.com/product/169">
Add to Cart
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/1512">
<img src="https://cdn-shop.adafruit.com/640x480/1512-00.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">Lock-style Solenoid - 12VDC</div>
<span class="product-price">$14.95</span>
<a id="1512-product" class="product-buy btn " data-pid="1512" data-qty="1" data-name="Lock-style Solenoid - 12VDC" data-price="14.95" href="https://www.adafruit.com/product/1512">
Add to Cart
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/1505">
<img src="https://cdn-shop.adafruit.com/640x480/1505-00.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">16mm Panel Mount Momentary Pushbutton - Black</div>
<span class="product-price">$0.95</span>
<a id="1505-product" class="product-buy btn " data-pid="1505" data-qty="1" data-name="16mm Panel Mount Momentary Pushbutton -  Black" data-price="0.95" href="https://www.adafruit.com/product/1505">
Add to Cart
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/830">
<img src="https://cdn-shop.adafruit.com/640x480/830-03.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">4 x AA Battery Holder with On/Off Switch</div>
<span class="product-price">$2.95</span>
<a id="830-product" class="product-buy btn " data-pid="830" data-qty="1" data-name="4 x AA Battery Holder with On/Off Switch" data-price="2.95" href="https://www.adafruit.com/product/830">
Add to Cart
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/914">
<img src="https://cdn-shop.adafruit.com/640x480/914-00.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">Adafruit Assembled Pi Cobbler Breakout + Cable for Raspberry Pi</div>
<span class="product-price">$6.50</span>
<a id="914-product" class="product-buy btn " data-pid="914" data-qty="1" data-name="Adafruit Assembled Pi Cobbler Breakout + Cable for Raspberry Pi" data-price="6.5" href="https://www.adafruit.com/product/914">
Add to Cart
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/64">
<img src="https://cdn-shop.adafruit.com/640x480/64-00.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">Half-size breadboard</div>
<span class="product-price">$5.00</span>
<a id="64-product" class="notify product-buy " data-pid="64" data-qty="1" data-name="Half-size breadboard" data-price="5.0" href="https://www.adafruit.com/product/64">
Out of Stock (Notify Me)
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/824">
<img src="https://cdn-shop.adafruit.com/640x480/824-05.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">Premium Female/Male &#39;Extension&#39; Jumper Wires - 40 x 12&quot; (300mm)</div>
<span class="product-price">$7.95</span>
<a id="824-product" class="product-buy btn " data-pid="824" data-qty="1" data-name="Premium Female/Male &#39;Extension&#39; Jumper Wires - 40 x 12&quot; (300mm)" data-price="7.95" href="https://www.adafruit.com/product/824">
Add to Cart
</a> </div>
</div>
<div class="product-wrapper">
<div class="product-image">
<a href="https://www.adafruit.com/product/1311">
<img src="https://cdn-shop.adafruit.com/640x480/1311-04.jpg" alt="" height="233" class="img-responsive">
</a> </div>
<div class="product-details">
<div class="product-title">Hook-up Wire Spool Set - 22AWG Solid Core - 6 x 25 ft</div>
<span class="product-price">$15.95</span>
<a id="1311-product" class="product-buy btn " data-pid="1311" data-qty="1" data-name="Hook-up Wire Spool Set - 22AWG Solid Core - 6 x 25 ft" data-price="15.95" href="https://www.adafruit.com/product/1311">
Add to Cart
</a> </div>
</div>
<div class="add-all-to-cart-container">
<a class="add-all-to-cart" href="#">Add All To Cart</a>
<div class="add-all-to-cart-progress"></div>
</div>
<div class="clear"></div>
</div>
</header>
</div>
</div>
</div>
<div class="related-guides-wrapper container">
<div class="row">
<div class="related-guides-title col-lg-12">
<h2>
RELATED GUIDES
</h2>
</div>
</div>
<div class="related-guides-content row">
<div class="14-guide masonry-block col-lg-3 col-md-3 col-sm-4 col-xs-12">
<div class="guide-block">
<div class="title-bar">
<div class="guide-type popular-guide">
<a href="/guides/popular">POPULAR</a>
</div>
<div class="title">
<h5>
<a href="/ttl-serial-camera">
TTL Serial Camera<br>
</a> </h5>
<div class="tagline">
<a href="/ttl-serial-camera">
Snap, Snap!
</a> </div>
<div class="author">by
<a href="/users/adafruit2">
<span class="name">lady ada</span>
</a> </div>
</div>
</div>
<a href="/ttl-serial-camera">
<img src='https://cdn-learn.adafruit.com/guides/images/000/000/014/medium310/397.jpg?1514389029' class='img-responsive guide-image' data-standard-image='https://cdn-learn.adafruit.com/guides/images/000/000/014/medium310/397.jpg?1514389029' data-mobile-image='https://cdn-learn.adafruit.com/guides/images/000/000/014/medium800/397.jpg?1514389029' />
</a> <div class="details">
<div class="description">
<a href="/ttl-serial-camera">
This guide is for our new TTL serial camera module with NTSC video output. These modules are a nice addition to a microcontroller project when you want to take a photo or control a video stream. The modules have a few features built in, such as the ability to change the brightness/saturation/hue of images, auto-contrast and auto-brightness adjustment, and motion detection.
</a> </div>
</div>
</div>
</div>
<div class="15-guide masonry-block col-lg-3 col-md-3 col-sm-4 col-xs-12">
<div class="guide-block">
<div class="title-bar">
<div class="guide-type popular-guide">
<a href="/guides/popular">POPULAR</a>
</div>
<div class="title">
<h5>
<a href="/el-wire">
EL Wire<br>
</a> </h5>
<div class="tagline">
<a href="/el-wire">
Working with Electroluminescent Wire
</a> </div>
<div class="author">by
<a href="/users/adafruit2">
<span class="name">lady ada</span>
</a> </div>
</div>
</div>
<a href="/el-wire">
<img src='https://cdn-learn.adafruit.com/guides/images/000/000/015/medium310/EL_Wire.jpg?1514389623' class='img-responsive guide-image' data-standard-image='https://cdn-learn.adafruit.com/guides/images/000/000/015/medium310/EL_Wire.jpg?1514389623' data-mobile-image='https://cdn-learn.adafruit.com/guides/images/000/000/015/medium800/EL_Wire.jpg?1514389623' />
</a> <div class="details">
<div class="description">
<a href="/el-wire">
EL Wire, also known as Electroluminescent wire, is a stiff wire core coated with phosphor and then covered with a protective PVC sheath. When an AC signal is applied to it, it glows a cool neon color. Find out how to solder, power, and work with EL Wire in your next project.
</a> </div>
</div>
</div>
</div>
<div class="16-guide masonry-block col-lg-3 col-md-3 col-sm-4 col-xs-12">
<div class="guide-block">
<div class="title-bar">
<div class="guide-type popular-guide">
<a href="/guides/popular">POPULAR</a>
</div>
<div class="title">
<h5>
<a href="/hacking-the-kinect">
Hacking the Kinect<br>
</a> </h5>
<div class="tagline">
<a href="/hacking-the-kinect">
Reverse engineering the Microsoft Kinect
</a> </div>
<div class="author">by
<a href="/users/adafruit2">
<span class="name">lady ada</span>
</a> </div>
</div>
</div>
<a href="/hacking-the-kinect">
<img src='https://cdn-learn.adafruit.com/guides/images/000/000/016/medium310/04a1fe47-8b58-41e9-a486-65456d2bf6ce_1.7d6bbbf694215ef00e24e2f11adddb89.jpeg?1514389899' class='img-responsive guide-image' data-standard-image='https://cdn-learn.adafruit.com/guides/images/000/000/016/medium310/04a1fe47-8b58-41e9-a486-65456d2bf6ce_1.7d6bbbf694215ef00e24e2f11adddb89.jpeg?1514389899' data-mobile-image='https://cdn-learn.adafruit.com/guides/images/000/000/016/medium800/04a1fe47-8b58-41e9-a486-65456d2bf6ce_1.7d6bbbf694215ef00e24e2f11adddb89.jpeg?1514389899' />
</a> <div class="details">
<div class="description">
<a href="/hacking-the-kinect">
Here&#39;s a step by step guide on how you can reverse engineer a Microsoft Kinect for the Xbox 360.
</a> </div>
</div>
</div>
</div>
<div class="17-guide masonry-block col-lg-3 col-md-3 col-sm-4 col-xs-12">
<div class="guide-block">
<div class="title-bar">
<div class="guide-type popular-guide">
<a href="/guides/popular">POPULAR</a>
</div>
<div class="title">
<h5>
<a href="/beaglebone">
BeagleBone<br>
</a> </h5>
<div class="tagline">
<a href="/beaglebone">
Tutorials for the TI embedded Linux board
</a> </div>
<div class="author">by
<a href="/users/adafruit2">
<span class="name">lady ada</span>
</a> </div>
</div>
</div>
<a href="/beaglebone">
<img src='https://cdn-learn.adafruit.com/guides/images/000/000/017/medium310/beaglebonetop_LRG.jpg?1448300904' class='img-responsive guide-image' data-standard-image='https://cdn-learn.adafruit.com/guides/images/000/000/017/medium310/beaglebonetop_LRG.jpg?1448300904' data-mobile-image='https://cdn-learn.adafruit.com/guides/images/000/000/017/medium800/beaglebonetop_LRG.jpg?1448300904' />
</a> <div class="details">
<div class="description">
<a href="/beaglebone">
New from the fine people who have brought us the Beagle Board, we now have a smaller, lighter, but powerful single board linux computer, Beagle Bone! We like this move to a more compact and integrated SBC. For example, there is onboard Ethernet and USB host, as well as a USB client interface (a FTDI chip for shell access). It even comes preloaded with Angstrom Linux on the 4 GB microSD card! Here are some tips and tricks to get your BeagleBone up and running.
</a> </div>
</div>
</div>
</div>
</div>
</div>
<div class="footer-spacer"></div>
</div>
<div class="modal fade" id="notify-modal">
<div class="modal-dialog">
<div class="modal-content">
<div class="modal-header">
<a href="#" class="close" data-dismiss="modal">×</a>
<h5>OUT OF STOCK NOTIFICATION</h5>
</div>
<div class="modal-body">
<p class="notify-modal-form-header"></p>
<div class="notify-modal-products"></div>
<form id="notify-modal-form" name="back_in_stock_notification">
<p class="notify-modal-form-notice"></p>
<div class="notify-modal-break"></div>
<div class="form-group">
<label class="inputLabel" for="name">YOUR NAME</label>
<input type="text" size="25" maxlength="64" name="name" value="">
</div>
<div class="form-group">
<label class="inputLabel" for="email">YOUR EMAIL</label>
<input type="email" size="25" maxlength="96" name="email" value="">
</div>
<input type="text" name="daigo" style="display:none;">
<input type="hidden" name="notify_me" value="true">
</form>
<div id="notify-modal-success" style="display:none">
<p>You have been successfully subscribed to the Notification List for this product and will therefore receive an e-mail from us when it is back in stock!</p>
<p>For security reasons, an e-mail has been sent to you acknowledging your subscription. Please remember that this subscription will not result in you receiving any e-mail from us about anything other than the restocking of this item.</p>
<p>If, for any reason, you would like to unsubscribe from the Notification List for this product you will find details of how to do so in the e-mail that has just been sent to you!</p>
</div>
</div>
<div class="modal-footer">
<a href="#" id="close-notify" style="display: none" data-dismiss="modal" data-target="#notify-modal">CLOSE</a>
<a href="#" id="submit-notify" rel="nofollow" class="blue-button">NOTIFY ME</a>
</div>
</div>
</div>
</div>
</div>
<footer id="adafruit-footer">
<div id="footer-content" class="container">
<div class="row">
<div class=" col-lg-6 col-md-6 col-sm-4 col-xs-12">
<nav>
<ul>
<li><a href="https://www.adafruit.com/contact_us">CONTACT</a></li>
<li><a href="https://www.adafruit.com/support">SUPPORT</a>
<li><a href="https://www.adafruit.com/distributors">DISTRIBUTORS</a></li>
<li><a href="https://www.adafruit.com/educators">EDUCATORS</a></li>
<li><a href="https://www.adafruit.com/jobs">JOBS</a></li>
<li><a href="https://www.adafruit.com/faq">FAQ</a></li>
<li><a href="https://www.adafruit.com/shippinginfo/">SHIPPING &amp; RETURNS</a></li>
<li><a href="https://www.adafruit.com/terms_of_service/">TERMS OF SERVICE</a></li>
<li><a href="https://www.adafruit.com/privacy">PRIVACY &amp; LEGAL</a></li>
<li><a href="https://www.adafruit.com/about">ABOUT US</a></li>
</ul>
</nav>
<div id="footer-copyright">
<a href="http://nytm.org/made-in-nyc/">ENGINEERED IN NYC</a> <span>Adafruit&nbsp;®</span>
</div>
</div>
<div class="col-lg-6 col-md-6 col-sm-8 hidden-xs">
<div id="footer-quote" class="">
"I think there's something strangely musical about noise"
<span class="quote-author">- <a href="http://en.wikipedia.org/wiki/Trent_Reznor">Trent Reznor</a></span>
</div>
</div>
<div id="footer-seals">
<img class="img-responsive" src="/logos/seals_2x.jpg" alt="Seals 2x" />
</div>
</div>
</div>
</footer>
</div>
</div>
<script>
    window.rails_env = 'production';
  </script>
<script src="/assets/application-8b5be248ee3af4b8548c7e83f8f4332713556aff09ca5904cf6857b662a57f95.js"></script>
<script type="application/ld+json">
    {
      "@context": "http://schema.org",
      "@type": "WebSite",
      "url": "https://learn.adafruit.com/",
      "potentialAction": {
        "@type": "SearchAction",
        "target": "https://learn.adafruit.com/search?q={search_term}",
        "query-input": "required name=search_term"
      }
    }
  </script>
</body>
</html>
