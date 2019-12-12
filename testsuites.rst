.. _test-suites:

Understanding Test Suites
=========================

.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline

A Test Suite is a collection of test cases that you would like to execute. When a test suite is submitted for a run, all test cases present within the test suite are executed.

A test suite can also be a logical grouping of test cases.

E.g. You can create test suites consisting of test cases that pertain to a Smoke Test or a Regression Test or one that groups together test cases specific to a module, say, payment, customer acquisition, order creation, etc.

  **a. Creating a test suite**
  
  1. Click on the Test Suites icon on theProject Dashboard. You are now on the 'Test Suite' page.
  
  2. Click on the 'Create Test Suite' button (i..e., the '*+*' icon) on the top right corner. The 'Create Test Suite' page opens up.
  
  3. On the 'Create Test Suite' page, enter a name and description for the test suite and hit the Enter key. You now see that the 'Add Test Cases' button is enabled. (*Note: Entering the test suite description is not mandatory*)
  
  4. Click on the 'Add Test Cases' button. 
     * You are now on the 'Modify Test Suite' page.
     * On this page you can see a list of all automation test cases that you have created.
     * You can search for a test case using the 'Search' text box provided, if required.
     * Once you have identified the test case or test cases you would like to execute, add them to the test suite by clicking on the green coloured 'plus' icon to the left of the test case name. On being selected the 'plus' icon changes into a red coloured 'minus' icon.
     * You can removea test case that has already been added by cicking on the red coloured 'minus' icon.
     * Test cases are executed in the order in which they are present in the test suite. You can change the order by dragging and dropping the test case entries in the test suite.
     * You can view the list of test cases you have selected by clicking on 'Show selected test cases'. Only the selected test cases are now displayed. This is how your final test suite would look like.
     * You can view the complete list of test cases at any time by clicking on the 'Show all test cases' button.
  
  5. Now that you have selected the required test cases, save your changes by clicking on the 'Save Test Suite Details' button at the top right. 

  You have now created a Test Suite!

  **b. Modifying Test Suites**

  All test suites that have been created are visible on the 'Test Suites' page.

  For each test suite, the following information is visible:  
  * test suite name 
  * test suite description 
  * name of the user who created the test suite
  * name of the user who last updated the test suite and the date and time of updation

  To the right side of each test suite entry there are a set of 'action' buttons provided. 

  Let's have a look at each of these buttons:

  :bolditalic:`Run Test Suite:` This option is denoted by the 'Play' button icon. Clicking enables the user to execute a test run. We shall cover this functionality in the ":ref:`create-test-run`" section

  :bolditalic:`Modify Test Suite:` You can add or remove test cases or rearrange their order in the test suite by cicking on this button

  :bolditalic:`Clone Test Suite:` This option enables you to create a copy of the test suite. You can then rename and modify the test suite as required.

  :bolditalic:`Delete Test Suite:` You can delete a test suite by ckicking on this button and providing confirmation.