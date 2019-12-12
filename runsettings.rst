.. _run-settings:

Run Settings
============


.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline


Whenever you start a new test session - whether Manual or Automation - there are certain default configuration values that are being used to determine the way your test session behaves.

'Run Settings' enable users to customise these default configuration values

You can create a new Run Setting by clicking on the 'Run Settings' icon on the Project Dashboard

RobusTest allows you to create 2 types of Run Settings:

1. Manual Runs Setting; and;
2. Automation Run Setting

**1. Manual Run Setting**

Manual Run Settings are used when starting a new Manual Test Session

A Manual Run Setting consists of only one kind of setting called 'General Settings'.

By default, the 'General Settings' section has the following parameters and values:

   a. Parameter: *reset* - default value: *no* - ensures that the app is not reset    

   b. Parameter: *uninstallAppAfterRun* - default value: *yes* - this ensures that the app is uninstalled from the device at the end of the test session

   c. Parameter: *uninstallAppBeforeRun* - default value: *yes* - this ensures that the app, if already installed, is uninstalled from the device at the beginning of a new test session

You can add/modify/delete other parameters to your run setting

**2. Automation Run Setting**

An Automation Run Setting is used while starting an Automation Test Session or when running automation tests.

The default automation run setting consists of the following 3 groups of settings:

   1. General Settings
   2. Automation Framework Settings
   3. Automation Notification Settings

   :bolditalic:`1. General Settings`

   This is the same as described for Manual Run Setting described above

   :bolditalic:`2. Automation Framework Settings`

   This section enables users to customise values for parameters to be passed to the Appium Automation Framework. This includes various *Appium Desrired Capabilities* such as '*automationName*', '*fullReset*', '*noReset*', etc.

   :bolditalic:`3. Automation Notification Settings`

   This section enables users to send out notification emails, at the end of a test run, to a group of email IDs 

   For each 'key' in the setting, the user can enter one or more email IDs in the 'Value' field separated by commas.

   There are 3 keys provided:

      a. *onComplete* - An email notification is sent to the the email IDs on completion of a test run

      b. *onFail* - An email notification is sent to the group of email IDs only if at least one test case, being executed as part of the run, has failed

      c. *onPass* - An email notification is sent to the group of email IDs only if all test cases being executed as part of the run have passed

  **Configuring Run Settings**

  Now that you have created a run setting, let's see how you can configure your test sessions to use a customised run setting

  :bolditalic:`a. Manual Test session`

    * Click on the 'Manual' icon on the Project Dashboard. The device selcetion screen now comes up.

    * While on the device selection dialog, clcik on the 'Configure Session' icon on the top right corner.

    * On the pop window that opens up, you will find a drop down called 'Run Settings'. You can select the Manual Run Setting that you would like to use by clicking on it in this drop down.

    * You can view the various key-value pairs in a selected run setting by clicking on the information icon to the right of the dropdown.

  :bolditalic:`b. Automation Test session`

    * Click on the 'Automation' icon on the Project Dashboard. The device selcetion screen now comes up

    * While on the device selection dialog, clcik on the 'Configure Session' icon on the top right corner.

    * On the pop window that opens up, you will find a drop down called 'Run Settings'. You can select the Automation Run Setting that you would like to use by clicking on it in this drop down.

    * You can view the various key-value pairs in a selected run setting by clicking on the information icon to the right of the dropdown.

  :bolditalic:`c. Automation Test Run`

    * Click on the 'Test Suite' icon on the Project Dashboard. 

    * Click on the 'Play' icon corresponding to the test suite you would like to execute

    * On the page that opens up, select the automation run setting of your choice from the 'Run Settings' drop down

    * You can view the various key-value pairs in a selected run setting by clicking on the information icon to the right of the dropdown.

