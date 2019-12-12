.. _test-session-session-management:

Test Session - Session Management
=================================

The vertical menu to the left of the test step table provides you various options regarding management of the test session

**1. Show Recorded Steps**

Tapping on this button displays the test step table. You can use this option to get back to recording your automation test steps, in case you had earlier moved away from it while using any of the options to be described below

**2. Session Information**

Clicking on this button provides you all details regarding the automation test session in progress. This includes information about:-

   a. the build - App name, build version, last uploaded, etc
   b. the device - Device name, ADB ID, OS version, etc,
   c. the project - Project name, Last build uploaded, etc

**3. Device Log**

You can view the logcat report in a tabular format with options to filter by the log level. You also have the option to download the log in CSV format.

**4. Run ADB command on device**

Sometimes, as part of your testing, you may want to run a few ADB commands on the device under testing. You can do so by clicking on the 'Run ADB commands on device' button.

This brings up the Command Line Interfce from where you can execute adb commands directly on the device.

**5. Copy session information**

Clicking on this button captures all relevant information about the session in progress onto the clipboard. This information includes information about when the test session began, details of the app build, details of the device being used, etc.

If you face an issue while in an automation test session, you can capture the session details using this option and then paste this  info in a support ticket that you log.


**6. Turn ON image-based element verification**

Clicking on this enables image-based verification. You can read more about this in the section on :ref:`image-based-verification`