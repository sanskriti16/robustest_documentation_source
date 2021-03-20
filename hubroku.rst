.. _hub-espresso:

Run Roku Tests
==============


RobusTest currently supports running of automation tests created using the JavaScript library.
Read more about the JavaScript Library here 

https://developer.roku.com/en-gb/docs/developer-program/dev-tools/automated-channel-testing/javascript-library.md

RobusTest provides a customization of the Roku JavaScript Library to enable running of test cases on the RobusTest device lab.
Download the library from the link below and use it place of the default Roku library

{RobusTest Device Lab}/v3/download/file/automated-channel-testing-master.zip


To run your tests on the RobusTest device lab you need to provide certain capabilities or information.
This information can be provided in the baseCapabilities.js file in the jsLibrary/library folder.

In the baseCapabilities.js file you need to provide the following values

1. Project ID - the RobusTest project ID 

2. Build ID - ID of the Roku built that has been uploaded to RobusTest

3. Job Identifier - A string to identify the job under which you are running this test case. This name will be used to group all the tests that are executed as part of a single job. So ensure that it is unique everytime you run the job but remains the same everytime you run a test case within a job.

4. Access Key - The unique access key generated for your user account

5. RobusTest Device Lab URL - The RobusTest device lab URL on which you shall run your tests. Ensure that you provide it in the format that is specified in the baseCapabilities.js file


In your test case, you shall define the following value

1. RobusTest Session Identifier - this will be used to uniquely identify your test case or test session assuming each test session is your test case

Note that the values that you provide in the baseCapabilities.js file can be over-ridden at your test case level.
Check the test_basic.js sample test case to understand better the writing of a Roku test case to run on RobusTest device lab







