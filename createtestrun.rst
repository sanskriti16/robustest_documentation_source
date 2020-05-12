.. _create-test-run:

Creating and Executing a Test Run
=================================

.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline


Now that we know how to create and modify a test suite, let us understand how to go about executing a test suite in a test run.

A test run constitutes of a combination of the following 5 components:-

a. *Test Suite*
b. *Run Settings*
c. *App build*
d. *Devices*
e. *Data sets*
f. *Run Mode* 

**a. Test Suite**

This is the primary componenet. It determines the group of automation test cases that will be executed in a test run. Creation of a test run begins by selecting the test suite to be run.

On the Test Suites page, click on the 'Run Test Suite' button (i.e., the '*Play button*' icon) for the test suite that you wish to execute. You are now on the 'Create Test Run' page.

**b. Run Settings**

Run Settings determine how your automation test run session is going to behave.

From the 'Run Settings' drop down, select the setting that you would like to use. If no custom Run Setting is used, then the 'System Default' run setting will be used. 

Details of a chosen Run Setting can be viewed by clicking on the 'information' icon to the right side of the 'Run Settings' drop down 

To know more about Run Settings, go through the :ref:`run-settings` page.

**c. App Build**

The 'Select Build' drop down displays a list of all the app builds uploaded to the project in which you created your automation test cases.

From this drop down, choose the right build version of the app on which you would like to execute your test cases.

**d. Devices**

One of the highlights of the RobusTest platform is its ability to execute a set of test cases on multiple devices in parallel.

On clicking on the 'Select Devices' drop down, you are provided with a list of devices on which you can run the test suite.

You can select a device by clicking on it in the dropdown. You can select multiple devices by clicking on each of those devices in the drop down.

Selected devices are visible in the 'Select Devices' field. Additionally, in the drop down, these selected devices are displayed in a blue coloured font.

Once a device is selected an entry is displayed on the 'Create Test Run' page corresponding to the selected device. This entry provides you information about the device name, the OS version running on the device, the device identifier and the dataset that is to be used for that specific device for the duration of the run. 

To *unselect* a selected device, perform any one of the following actions:

* click on the same device in the drop down for a second time; *or*
* delete the entry corresponding to this device in the 'Select Devices' field using the keyboard; or;
* on the list of device rows displayed below the 'Select Devices' drop down, click oin the 'Remove Selected Devices' button for the entry corresponding to the device to be removed from the run.

**e. Data sets**

Data sets are used to execute test cases on data values that are different from that used originally when these test cases were first created.

As mentioned above, for each device selected for a run, an entry is created and displayed below the 'Select Devices' dropdown.

On this entry is displayed the data set that is to be used while executing the test run on this device.

The data set drop down displays a list of all data sets that were created in the project in which the autoamtion test cases were created. You can choose the data set of your choice from this dropdown. 

If you do not specifically select a data set, then, the 'Original' data set, that was created by the system, is selected by default and the same will be used during the course of execution of the test run.

Details of the data set chosen can be seen by clicking on the 'View Data Set' button on the same row.

To know more about data sets, read the '*Using Datasets*' section of the :ref:`data-parameterisation` page.

**f. Run Mode**

Test runs can be executed in one of two modes:

  *1. Parallel*
  
  *2. Distributed*

  **1. Parallel Run Mode**

  * In this mode, :bolditalic:`all` test cases in the test suite are executed on :bolditalic:`each` device that has been selected for the run.
  * This mode is helpful in improving device coverage for your tests.

  **2. Distributed Run Mode**

  * In this mode, the test cases in the test suite are distributed among the devices that have been selected for the run and then executed.
  * Initially each device is given a different test case for execution. 
  * When a test case has been executed to completion, the device is free. This device is then provided another test case from the test suite for execution.
  * This mode is useful in increasing the speed of execution of your tests, resulting in fater turnaorund.