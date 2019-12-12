.. _hub-xctest:

Running test cases on XCTest
============================

**1.** Identify the project which you shall use for running your tests. If you do not already have such a project, then you need to first create a project. Once identified, note down the Project ID for the project.

  * This needs to be done only once. 
  * *Project ID* is the alphanumeric number in the URL of the project dashboard.

**2.** Upload the app enterprise build to your project and note down the build ID.

  * This needs to be done everytime you have a new app build. 
  * *Build ID* is the name of the file that you get when you copy the URL to the build.

**3.** Upload the zipped up xctest file to your project and note down the build ID.

  * This needs to be done everytime along with a new app enterprise build. 
  * Build ID is the name of the file that you get when you copy the URL to the build. Let's refer to this as the *Test Build ID*.

**4.** Get your ACCESS KEY from your profile page in RobusTest.

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

