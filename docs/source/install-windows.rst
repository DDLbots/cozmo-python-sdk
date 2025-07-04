.. _install-windows:

######################
Installation - Windows
######################

This guide provides instructions on installing the Cozmo SDK for computers running with a Windows operating system.

^^^^^^^^^^^^^^^^^^^
Installation Videos
^^^^^^^^^^^^^^^^^^^

For your convenience, videos are provided showing the installation steps being followed on a Windows computer; one using an iOS device, and one using an Android device. There is also full text-based documentation below these.

.. raw:: html

   <iframe width="690" height="388" src="https://www.youtube.com/embed/gtRS3iqzSuA?rel=0" frameborder="0" allowfullscreen></iframe>

   <iframe width="690" height="388" src="https://www.youtube.com/embed/9TJeK_AEFYo?rel=0" frameborder="0" allowfullscreen></iframe>   

|

^^^^^^^^^^^^^^^^^^^
Python Installation
^^^^^^^^^^^^^^^^^^^

Download the `Python 3.5.1 (or later) executable file from Python.org <https://www.python.org/downloads/>`_ and
run it on your computer.

.. important:: We recommend that you tick the "Add Python 3.5 to PATH" checkbox on the Setup screen.

^^^^^^^^^^^^^^^^
SDK Installation
^^^^^^^^^^^^^^^^

**Important: In 2025 and later, the Cozmo SDK requires a local dependency named ``cozmoclad`` that is no longer available from PyPI.**

You **must** install it manually before continuing.

1. Open Command Prompt or PowerShell, then run the following to download `cozmoclad`::

    curl -o cozmoclad-3.6.6-py3-none-any.whl https://raw.githubusercontent.com/DDLbots/cozmo-python-sdk/refs/heads/master/cozmoclad/cozmoclad-3.6.6-py3-none-any.whl

2. Then install it::

    pip3 install --user .\cozmoclad-3.6.6-py3-none-any.whl

3. Finally, install the SDK itself::

    pip3 install --user "cozmo[camera]"

Note that the `[camera]` option adds support for processing images from Cozmo's camera.

"""""""""""
SDK Upgrade
"""""""""""

To upgrade the SDK from a previous install, follow these steps:

1. **Uninstall the old version of `cozmoclad`**::

    pip3 uninstall cozmoclad

2. **Download the latest `cozmoclad` wheel**::

    curl -o cozmoclad-3.6.6-py3-none-any.whl https://raw.githubusercontent.com/DDLbots/cozmo-python-sdk/refs/heads/master/cozmoclad/cozmoclad-3.6.6-py3-none-any.whl

3. **Reinstall `cozmoclad`**::

    pip3 install --user .\cozmoclad-3.6.6-py3-none-any.whl

4. **Upgrade the SDK**::

    pip3 install --user --upgrade cozmo

^^^^^^^^^^^^^^^^^^^
Mobile Device Setup
^^^^^^^^^^^^^^^^^^^

* **iOS** devices require `iTunes <http://www.apple.com/itunes/download/>`_ to ensure that the usbmuxd service is installed on your computer. Usbmuxd is required for the computer to communicate with the iOS device over a USB cable. While iTunes needs to be installed, it does not need to be running.

* **Android** devices require installation of :ref:`adb` (adb) in order to run the Cozmo SDK. This is required for the computer to communicate with the Android mobile device over a USB cable and runs automatically when required.

^^^^^^^^^^^^^^^
Troubleshooting
^^^^^^^^^^^^^^^

Please see the :ref:`trouble` section of the Initial Setup page for tips, or visit the `Cozmo SDK Forums <https://forums.anki.bot/>`_ to ask questions, find solutions, or for general discussion.

----

`Terms and Conditions <https://anki.bot/policies/terms-of-service>`_ and `Privacy Policy <https://anki.bot/policies/privacy-policy>`_

`Click here to return to the Anki Developer website. <http://developer.anki.bot>`_
