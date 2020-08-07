.. _test-step-details:

Test Step Details
=================

For any recorded test step, if you click on the 'Show Step Details' button, you can see that the test step expands to reveal the following tabs:

1. Basic
2. Settings
3. User Data
4. Return Data
5. XPath
6. Script 
7. References 
8. Dependencies
9. Function Steps

These tabs provide you more information about and control over the automation test steps you have created. Let's have a look at each of these tabs in detail.

**1. Basic** 

This tab let's you provide a name and a description for the test step that has been recorded.

Whenever you record a test step, by default, RobusTest provides you a test step name depending on the element and the action that was performed. Sometimes, this default test step may not be easy to understand. E.g. a step named 'Tap on Relative Layout'.

In such cases, the user can go to the Test Step Name field under the 'Basic' tab and rename the step to something more intuitive and meaningful. E.g. 'Tap on Play button icon'

**2. Settings**

For test steps that record a user action such as a tap, type, swipe, etc, the 'Settings' tab provides certain configurable paramters.

* *onFail* - This prameter determines what action should be performed at the end of execution of a test step. 

  This field can have the following values:

   * *Fail* - This is the default value. If the test step is not executed successfully, the succeeding test steps *are not* executed and the test case is considered to have failed.
   * *Continue* - In this case, even if the test step is not executed successfully, the succeeding test steps *are* still executed.  and the test case is considered to have failed.

* *waitforElement* - This time parameter (in units of seconds) indicates the period of time RobusTest will wait to find the element on which an action has been recorded in the current test step. This value will override the default value set for automation at the platform level. You can modify this value to increase or decrease the time taken to find this element.

* *failType* - 

* *messageOnFail* - 

**3. User Data**

The data that you enter while recording a 'Type' test step is separated out from the script and displayed here. This enables you to change the data and execute the same test step without having to re-record the same.

More details on how to manipulate the user data is available in the :ref:`data-parametrisation` section 

**4. Return Data** 

In general, this tab provides info on the position of an element on the device screen. It provides you the top, bottom, left and right bounds as well as the length and width of the element.

If the element contains a 'text', the value of the text attribute is displayed.

The most important use of the return data section is in the case of a 'Store' and 'Verify' operation.

All details of the element stored are available on the Return Data tab. This data can then be used for verification purposes in a later test step. For more details please see the section on :ref:`verification-main-page`

**5. XPath** 

The xpath of the object or element on which an action was performed is visible on this tab.

The default Xpath created at the time of recording the test step is referred to as the 'Original' xpath.

On clicking on the 'Add New Xpath', you can modify the existing Xpath by either:

a. adding more attributes to it (by selecting the checkbox next to the attribute being added); or

b. editing the Xpath manually

On providing a new name and clicking on the 'Save' button, the modified Xpath is saved. 

Let us have a look at the various operations you can now do on the Xpaths.

* 'Edit Xpath' - This enables you to edit the Xpath selected in the Xpath drop down. The 'Original' Xpath can never be edited.

* 'Copy Xpath' - This copies the selected Xpath to the clipboard for later use

* 'Delete Xpath' - This enables you to delete the selected Xpath. The 'Original' Xpath can never be deleted.

* 'Make Default' - This is a very interesting option. Let's say, after recording an action on an element, you have edited the Xpath to make it uniquely identifiable. It is now highly desirable to use this unique Xpath to identify this element in each test step it is being used. You can ensure this by clicking on the 'Make Default Xpath' button. Thereafter, this element will be identified by the newly created unique Xpath. 

**6. Script** 

This tab shows the test script to be executed when the automated test step runs. The script is shown in a smart script editor. If the user wishes to add custom code to his/her test scripts, s/he can do that in this script editor. The editor also checks for syntax correctness.

**7. References** 

Please refer to the section on :ref:`data-parametrisation`

**8. Dependencies**

Please refer to the section on :ref:`data-parametrisation`

**9. Function Steps**

This tab is visible only in a test step where a function is being executed. It provides you the following details:

* the name of the function being called
* the name of the test case that was converted into this function
* a list of the different test steps that will be executed as part of this function

