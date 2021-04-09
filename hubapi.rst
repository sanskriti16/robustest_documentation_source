.. _hub-api:

Run API tests using Karate
==========================

.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline


Karate is a test automation framework that can be used to perform API testing.

If your organisation uses Karate to test your APIs, then RobusTest provides you a way to push your test results to RobusTest so that you can see your run reports in one place.

**Pre-requisites:​**

**1.** Apache Maven should be installed on your laptop (or on the server from where you are going to execute your tests)

**2.** The path to Apache Maven's '*bin*' folder should be added to your machine's *PATH* environment variable

   * if not added, you can do the same using the following command:

     * export PATH=$PATH:<path to Apache Maven bin folder>

**Steps for set up and execution:**

**1.** Obtain the latest version of the '*karate-robustest-demo*' folder

   * On request, RobusTest provides you with a special Karate folder as a zip file.
   * Download this zip file.
   * Unzip the file.
   * You will now see a folder called '*karate-robustest-demo*'.

**2.** On Terminal, go to the folder '*karate-robustest-demo/src/test/java*'.

​
**3.** Open the file named **reportportal.properties** in edit mode and provide appropriate values for the following fields:
   * **rp.endpoint**

     * this will point to the robustest hub url
     * it will be of the form: *<RobusTest URL>/v2/hub* 
   * **rp.launch** 
   
     * You can provide any custom string in this field. It will act as an identifier for your API job. 
     * All test cases that should be displayed under the same job should have the same value for this field.
   * **rp.project**
   
     * This will be the project ID of the RobusTest project in which you will be running your API report jobs
   * the *accessKey* parameter in **rp.attributesfield**
   
     * You can get your access key from your profile section on RobusTest

**4.** Place your feature files in the *karate-reportportal-demo/src/test/java/features* folder

**5.** Executing your API Tests:
   * Go to the *karate-reportportal-demo* folder and run the command **mvn clean test​**
   * This command cleans your 'target' folder and then executes your tests.
   * You should now see a job being executed in the Test Runs page of your RobusTest project.

**6.** Viewing your reports
   * On clicking on the job, you can see further details about the various API tests being executed
   * On clicking on an API test name you will reach the API test details page. Here: 

     a. you can find information about your test at a test step level
     b. you have the option to veiw the Karate logs


**Grouping API Tests**

* Sometimes you may want to group your tests under one or more tags. E.g. Payments, Login, Smoke, Regression, etc.
* You may want to use such tags to view only API tests relevant to you.
* RobusTest provides you a way to group your API tests the way you want.

**1.** In each feature file, provide the group name as an annotation in the first line : E.g. *@movie*

   * You can also provide more than one Test Group names separated by a space. E.g. *@movie @smoke* 
   * See the screenshot below for an example:

 .. image:: _static/testgroup.png
 	:align: center

**2.** Now run your tests using the command: *mvn clean test​​​​*.

**3.** Go to the 'Test Cases' section of the job run report on RobusTest.

**4.** You can now use the '*Search*' bar to search using the Test Group required. E.g. on searching with '*movie*', all test cases that come under the 'movies' group are listed.