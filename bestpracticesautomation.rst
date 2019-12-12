.. _best-practices-in-automation:

Best Practices in Automating Tests using RobusTest
==================================================

.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline

**1. Name test steps appropriately**

* When recording a test case, RobusTest automatically generates test steps based on the actions performed. Test steps are created with the intention of being easily understandable.

* However, in many cases the test steps are not intuitive because of various reasons e.g. no content-desc provided for the element. 

* It is, therefore, recommended that the test steps are reviewed and checked for easy understanding for all users. In case required, test steps can be easily renamed.

* This will help in :-
   * easily understanding the test case
   * faster and easier debugging of errors from the functional reports

     E.g. the default step name that says 'Tap on Relative Layout'. This makes it difficult to understand from the reports or from the test script on what the intended action is. 

     Instead, the test step should be renamed in a more meaningful manner such as 'Tap on the option Recharge'.

**2. Use functions wherever possible**

* RobusTest enables creation of functions out of existing test cases. This is a powerful feature that helps in reducing the time & effort to automate. It also enables easy maintenance and update of test code in case of changes in the mobile application.

* Use functions wherever a series of steps form a logical unit, e.g. series of steps that capture customer data, selecting a usage plan, selecting a rental plan, etc.

* For actions that are repeated across more than one test scenarios, the use of functions helps with re-usability, thereby reducing the time spent in automation.

* Using functions will significantly reduce the amount of future time spent in incorporating changes to app flows, data, element resource ids, etc.

* At the very minimum have one function to capture the actions performed on each screen of the app. 

* You can break this down further based on how a particular app screen is structured. Eg., on a single page where you are entering customer details, capturing images, selecting a number, etc, each can have a function of its own. The 'customer details' function can itself be broken down into functions for 'personal details', customer address', etc. as applicable

  E.g. Say, there are a series of standalone test steps (i.e., test steps not inside a function) where a 4G Plan is being selected and that these steps are repeated in a number of test cases. In future, if the specific plan being selected changes, you would have to go to each and every test case and update them. 

  Instead, have these steps within a function named ‘Select Rental Plan’. Now, any change in the way a rental plan is created would only require a one time change within this function script. This change is reflected in all test cases that call this function.

**3. Perform a ‘Swipe’ action in small increments**

* While automating a ‘Swipe Up’ or a ‘Swipe Down’ action, it is recommended to do so in small incremental movements, instead of one single long swipe across the screen. This would ensure that the same automation script will work across device screens of different sizes.

**4. Use the element attributes to define better XPaths**

* RobusTest is designed to create highly accurate and robust XPaths for elements in the mobile app. However, in certain cases the auto-generated XPaths may not work due to various reasons e.g. duplicate resource ids, non-existing resource ids.

* When tapping on a button or a link with a text, which is not subject to frequent changes, it would be a good practice to improve the XPath by adding to it element attribute values that can help in identifying the element uniquely e.g. ‘text’ or ‘content-desc’.
 
* The XPath, thus modified to make it further unique, makes it easier to identify elements when the resource id is not unique or non-existent.

**5. Use the ‘Find Concurrent Elements’ functionality**

* Often times  we find multiple elements overlaying one another around the same geographical area within a screen of an app. Using the ‘Find Concurrent Elements’ option will help in this scenario to identify the correct element that the user wants to perform an action on.

* Using the ‘Find Concurrent Elements’ option will display a list of elements that occupy the area within the app where the user has performed a left-click action. Select the required element and click on ‘OK’. Now, any subsequent action performed, such as Tap, Store, Verify, etc, is done on the element selected in the previous step from the list.

**6. Use meaningful names for Stored variable**

* When storing a value in a variable, ensure that the variable name is something meaningful and unique. 

  E.g Initial Data Balance for Postpaid, Customer First Name, etc. This makes it easier to pick the right variable when doing a verification against it.

**7. Mention the variable name in test step while using the ‘Store’ option**

* When using the ‘Store’ option to store a value in a variable, by default, the test step gets generated with a description in the format: Store <value> for later verification.

  E.g. Store “10” for later verification  <- Here 10 may be the initial data balance in GB for a postpaid customer

* Mentioning the variable name in the test step makes it easier to understand the test script and the functional reports. E.g. Store initial postpaid data balance for later verification

**8. Provide proper descriptions for test cases**

* While saving an automation test script, ensure that a meaningful name and description is provided. 

* When a test case fails, a relevant description helps the user to identify the business flow correctly without spending too much time on it.

* In the ‘Test Cases’ page, the user can search for a test case based on test case name and test case description. A meaningful description goes a long way in identifying the test case and reducing the time spent in looking for it

**9. Name functions appropriately**

* When converting a test case into a function:-
   * give the function a name that makes its purpose very clear to all users

   * name it in a way that the test case name/description can be easily associated with the function name. This helps if the user wants to make a change in the function and is looking for the corresponding test case


**10. Use Reports for debugging functional and performance issues**

* The Functional and Analytic reports can help a lot in debugging errors in scripts


  :bolditalic:`a. Functional Reports`

     * The error message at the top of the functional report for a test case run tells you why the test case failed.
     * The test step at which the test case failed can be seen in ‘Red’. 
     * Make sure you have a look at the test step and screenshot just before the above failed step. Often the real reason for failure can be observed in this step.

  :bolditalic:`b. Analytic Reports`

     * If you observe that the app suddenly gives way to the device Home screen, have a look at the device logcat section within the Analytic report
     * Go to the section named ‘Log’ under Analytic report and scroll down to the bottom. If the last few entries in this section show that the app is being closed or a ‘Kill App’ instruction is being executed, it means that the App is crashing at this point.
     * If the App seems to be taking an inordinately long period of time to load a page or transition between screens, have a look at the usage of CPU, Memory, Network, etc. This would provide the developers an idea on where to focus on to improve the app performance.
     * Look at the number of external calls to the Garbage Collector (GC). A huge number of external GC calls within a small time period indicates inefficient usage of memory leading to slower performance of the app.
