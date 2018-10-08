THETA Plug-in Development Quickstart
####################################

.. toctree::
   :maxdepth: 1
   :caption: Contents:

Overview
========

1. `Join the partner program <https://api.ricoh/products/theta-plugin/>`_ (it's free as of Oct 2018)
2. Enable THETA developer mode - Use RICOH desktop application on Mac or Windows
3. Download one of the many code examples from GitHub - My personal favorite starting place is `THETA Sample Plug-in: CameraAPI Capture Plugin <https://github.com/ricohapi/theta-plugin-camera-api-sample>`_
4. Open project in Android Studio
5. Build apk and install into THETA V with a USB cable and adb
6. Use `Vysor <https://www.vysor.io/>`_ to set application permissions
7. Start plug-in using Vysor. Test it

Testing Plug-in Untethered
--------------------------

After you set the permissions with Vysor, you need to complete the following steps:

1. Set the default plug-in to launch using the Ricoh mobile app or the Ricoh desktop app
2. Put camera into plug-in mode by pressing the lower mode button for more than 2 seconds. 
   The LED above the shutter button will turn white.

Resources and Help
==================
* `RICOH THETA Plugin Development Guide <http://theta360.guide/plugin-guide/>`_ (Community)
* `THETA Plug-in User Guide <http://theta360.guide/plugin-user-guide/>`_ (Community)
* `Official API Documentation <https://api.ricoh/docs/theta-plugin/api/?utm_source=theta360guide>`_ (RICOH)
* `Community Discussion <https://community.theta360.guide/c/theta-api-usage/plugin>`_ (Community)


Main Code Examples
==================
You can develop custom functionality for RICOH THETA V 
cameras in minutes by downloading an existing open source 
plug-in and modifying it for your specific requirements.
Here are 8 plug-ins that will get your development started like a 
rocket.

Cloud Upload 
------------
* Upload automatically from THETA to Google Photos for 360 and VR viewing
* Author: Ricoh
* `GitHub <https://github.com/ricohapi/theta-cloud-upload-plugin>`_

Wireless Live Streaming
-----------------------
* 4K equirectangular live streaming from THETA direct to YouTube and Facebook using RTMP
* Author: Ricoh
* `GitHub <https://github.com/ricohapi/theta-wireless-live-streaming-plugin>`_

Automatic Face Blur
-------------------
* Automatically detect and blur the faces of people to protect privacy
* Author: Ricoh
* `GitHub <https://github.com/ricohapi/theta-automatic-face-blur-plugin>`_

Live Streaming Plug-in Sample for RICOH THETA
---------------------------------------------
* Sample application using WebRTC SFU to live stream spherical video to the 
  RICOH Cloud with the `RICOH Live Streaming API <https://api.ricoh/products/live-streaming-api/>`_
  for their cloud. 
* Author: Ricoh
* `GitHub <https://github.com/ricohapi/theta-plugin-ricoh-live-streaming-sample>`_

THETA Sample Plug-in: CameraAPI Capture Plugin
----------------------------------------------
* Excellent starting point for using the internal CameraAPI to take pictures and video. Simple and easy to customize. 
* Author: Ricoh
* `GitHub <https://github.com/ricohapi/theta-plugin-camera-api-sample>`_

THETA Sample Plug-in: WebAPI Capture Plugin
-------------------------------------------
* Great sample application to use the WebAPI from the plug-in
* Author: Shohara
* `GitHub <https://github.com/theta360developers/theta-plugin-web-api-sample>`_ 

Dual-fisheye Plug-in
--------------------
* Ichi Hirota's dual-fisheye plug-in to take 3 bracketed images. Includes examples for modifying 
  exposure and the number of images
* Author: Ichi Hirota
* `GitHub <https://github.com/theta360developers/original-dual-fisheye-plugin>`_ 

THETA Plug-in SDK
-----------------
* Official plug-in SDK
* Ricoh
* `GitHub <https://github.com/ricohapi/theta-plugin-sdk>`_ 

More Code Examples
==================

Here are three additional plug-ins from the community. These are all based on the 
`THETA Sample Plug-in: Camera API <https://github.com/ricohapi/theta-plugin-camera-api-sample>`_
project listed above.

Long 2K Video
-------------
* Bypasses 25 minute video recording limitation to record 1 hour and 24 minutes 
  of 2K video with spatial audio
* `GitHub <https://github.com/theta360developers/long-2k-video>`_

Long 4K Video
----------------------------------------------------------------------
* Tested to 1 hour 24 minutes of 4K 30fps video with mono audio and 48 minutes 
  with spatial audio and default encoding.
* `GitHub <https://github.com/theta360developers/4k-long-video>`_

Surveillance 2K
---------------
* 10 hour 55 minute saved to internal storage. 2K, 10fps
* `GitHub <https://github.com/theta360developers/surveillance-2k>`_ 


Live Streaming Tips
===================


Facebook, YouTube, Periscope and RTMP
-------------------------------------
Facebook, YouTube, and Periscope use Real-Time Messaging Protocol (RTMP) to live 
stream events. The 
`Wireless Live Streaming Plug-in <https://github.com/ricohapi/theta-wireless-live-streaming-plugin>`_ 
provides a great example of RTMP for 4K equirectangular video direct from the camera.

WebRTC, Oculus Go and Video Conferencing
----------------------------------------

You will need to do more work for WebRTC. The 
`RICOH Live Streaming plug-in Sample for RICOH THETA <https://github.com/ricohapi/theta-plugin-ricoh-live-streaming-sample>`_
provides a complete open source example using the RICOH Cloud servers.

If you want to use WebRTC with your own servers, you will need an external signaling server.

Examples of WebRTC external server use:

* `HowTo: Viewing 360° Video in Real-Time from THETA V with Oculus Go Browser <https://community.theta360.guide/t/howto-viewing-360-video-in-real-time-from-theta-v-with-oculus-go-browser/3066>`_
* `Making Theta 360 work with OpenTok’s client-side webRTC livestreaming - mobile stitching - google “cardboard” view <https://community.theta360.guide/t/making-theta-360-work-with-opentoks-client-side-webrtc-livestreaming-mobile-stitching-google-cardboard-view/986>`_
* `360 Video Conferencing with the RICOH THETA S <https://community.theta360.guide/t/360-video-conferencing-with-the-ricoh-theta-s/38>`_

Ethernet
--------

Although the Wireless Live Streaming plug-in does work with Ethernet, the camera cannot be powered by 
Ethernet.  There is no known success of bypassing the battery to power the THETA V from an external 
source. If you use Wi-Fi, you can power the THETA V from the USB port

Heat
----

HoloBuilder has reported success with 24 hour 4K live streaming using Wi-Fi. Some people have reported heat issues.

* blowing a fan on the body of the camera helps. You can use a household fan and angle it toward the camera.
* Using Wi-Fi will generate more heat than streaming through the USB cable
* Although you can stream dual-fisheye and offload the stitching, Ricoh does not release lens parameter information.

USB
---
No one has figured out how to stream from the plug-in over USB as of Oct 2018.  We do not think it 
is possible to stream from the plug-in using USB. We recommend that you use the 
normal camera application and not the plug-in. 

Power
-----
We're using a mobile phone charger capable of supplying 1.5 amps for our tests.  Do not 
power the camera from your computer USB while attempting Wi-Fi streaming.  
Although the camera is receiving power from the USB when it is streaming over Wi-Fi, 
our initial tests indicate that the battery power may be decreasing slowly.  

Test and Debug
--------------
Tip to use adb with a USB cable and Wi-Fi for streaming

.. code-block:: bash

  adb shell settings put global usb_debug true


Use adb from IP address
-----------------------

If you're testing Wi-Fi live streaming, you may be trying to connect  the THETA V Wi-Fi to the Internet while you are debugging the plug-in with Vysor  or adb connected to your camera with a USB cable. This won't work.

To get Vysor or adb to work with TCP/IP, you need to run the following command first with the camera connected with a USB cable:

.. code-block:: bash

  adb tcpip 5555


Get IP address from router.

Once connected, establish adb connection with:

.. code-block:: bash

  adb connect IP.address:PORT


or with my IP address of 192.168.2.102

.. code-block:: bash

  adb connect 192.168.2.102:5555

You can also use Vysor with an IP address that is established using Wi-Fi or Ethernet.

---

`Join the THETA Partner Program to Start Building Your Own Plug-in <https://api.ricoh/products/theta-plugin/>`_




