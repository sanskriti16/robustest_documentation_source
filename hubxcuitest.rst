.. _hub-xcuitest:

XCUITest
========

**1.** Identify the project which you shall use for running your tests. If you do not already have such a project, then you need to first create a project. Once identified, note down the Project ID for the project.

  * This needs to be done only once. 
  * *Project ID* is the alphanumeric number in the URL of the project dashboard.

**2.** Upload the app enterprise build to your project and note down the build ID.

  * This needs to be done everytime you have a new app build. 
  * *Build ID* is the name of the file that you get when you copy the URL to the build.

Refer to the Upload Build - Remote section in the following link for build upload API 

http://docs.robustest.com/en/latest/projectdashboard.html

**3.** Upload the zipped up xctest file to your project and note down the build ID.

  * This needs to be done everytime along with a new app enterprise build. 
  * Build ID is the name of the file that you get when you copy the URL to the build. Let's refer to this as the *Test Build ID*.

Refer to the Upload Build - Remote section in the following link for build upload API 

http://docs.robustest.com/en/latest/projectdashboard.html

**4.** Get your ACCESS KEY from your profile page in RobusTest.

Refer to the following link to get help with getting your Access Key

https://robustest-docs.readthedocs.io/en/latest/userprofile.html

**5.** Once you have the three pieces of information above, invoke the test using the following API details:

* *URL:* **<RobusTest URL>/v3/xcuitest/job/new?accesskey=<ACCESS KEY>**

* *METHOD:* **POST**

* *PAYLOAD:*

::

   { 
     "identifier":"<IDENTIFIER_NAME_GIVEN_BY_ENTERPRISE>",
     "deviceVersion":"<iOS version of the device>",
     "project":"<Project ID>",
     "build":"<Build ID>",
     "testBuild":"<Test Build ID>"
   } 

**6** When you run your job using the API above, the response will contain the job id in form of the key _id. Use this value to get the JSON for the run report

http://<RobusTest URL>/v3/report/<job id>/xcuitest

**7** To get the JSON report for an individual test case, use the id value for each test case run instance in the following URL

http://<RobusTest URL>/v3/xcuitest/testcase/<test case instance ID>