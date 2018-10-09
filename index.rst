THETA Plug-in Development - Getting Started
####################################

.. toctree::
   :maxdepth: 1
   :caption: Documents:


   examples/main
   examples/additional
   streaming/tips
   

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
