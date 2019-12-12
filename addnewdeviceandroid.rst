.. _adding-new-devices-android:

Adding new devices to RobusTest - Android
=========================================


.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline


When adding a new Andorid device to the RobusTest platform for the first time, you need to first prepare the device by performing the following set of actions on it:

1.  Turn on Developer Mode

    * Go to the 'About Phone' section under Settings on your mobile device
    * Now, tap on the build number field 7 times continuously to turn on 'Developer Options'

2.  Stay Awake should be turned on

3.  USB Debugging should be turned on

4.  Allow mock locations

5.  Set USB connection behavior to act as media device

6.  Set location as only GPS (option may be “only device” on some devices)

7.  Remove any lock screen

8.  Security settings - Allow installation from unknown sources

9.  Set as true “Do not verify apps installed over USB”

10. Display - Set rotation as off

11. Display - Set screen timeout to Never (in case Never is not an option set it to maximum possible time available)

12. Once the above steps are completed, plug the device into the node server through a USB cable. Make sure you use a good quality 
cable for better data transfer, reliable connectivity and better device charging.

13. Upon connecting the device, an alert message with the title “Allow USB Debugging?” should show up on the device screen. Select the checkbox to “Always allow from this computer”. Tap on OK on the device

14. Once the device is plugged in, the system will take upto 2 minutes to identify the device and add it to devices list.

15. Confirm that you are able to view the device in your device list from manual and automation testing.

**Additional Steps for Xiaomi or MI devices:**

:bolditalic:`Instructions for Mi/Xiaomi devices`

:bolditalic:`1.Security App`

a. Tap on the Security App
b. Tap on the Permissions Icon 
c. Tap on the Settings icon on the top right
d. Make sure Install via USB is TURNED OFF


For new device models:

a. Tap on the Security App
b. Tap on the Settings icon on the top right
c. Tap on 'Security Scan'
d. Disable 'Scan before installing'
e. Disable 'Auto-updates'
f. Disable 'System Updates'


:bolditalic:`2. Developer Settings`

a. Tap on Settings
b. Tap on Additional Settings
c. Tap on Developer Options
d. Developer Options - TURN ON
e. USB Debugging - TURN ON
f. Install via USB - TURN ON
g. USB Debugging (Security Settings) - TURN ON
h. Verify apps over USB - Turn OFF
i. Turn on MIUI Optimization - TURN OFF

:bolditalic:`3. Privacy`

 
a. Tap on Settings
b. Tap on Additional Settings
c. Tap on Privacy
d. Unknown Sources - TURN ON

----------------

*P.S. Some older MI devices may have only one of the above options (i.e., i and ii) available and/or may be named differently. Enable the relevant option*
