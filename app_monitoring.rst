App Monitoring
==============

Using RobusTest, you can create an App Monitor. An App Monitor continuously monitors a specific screen of your app for changes in the page elements. This is great for monitoring apps in production.

Creating an App Monitor

1. An App Monitor can be seen as a special case of a RobusTest Automator Test Case
2. An App Monitor test case will consist of three functions

a. Setup
b. Setup App State
c. Monitor


Setup & Setup App State functions

The Setup function & Setup App State function work together to bring the app to the state/screen which needs to be monitored. What is the difference between the two and the need for the two you may ask.

If while running the App Monitor, the app crashes or the app needs to be brough back to the screen because of screen stuck, then the system will use the test steps in the SetApp State to come back to the screen.

If while running the App Monitor, the monitoring process as a whole crashes or errors out, then the system will need to start the whole process from the start including logging into the app or similar steps which will be required for a fresh install. In such a case the Setup and Setup App State functions will both be run in that order.

Monitor function

The Monitor function contains the steps which specify which elements on the screen need to be monitored.
To create a monitor step, click on the Monitor button on the upper toolbar in the Automator session
Provide values for the various fields in the pop up dialog

Event Name

Event Description

Event XPath

Restart Monitor Timeout

Detect Event


Now create new test case with the following steps

Step 1: Setup function
Step 2: Setup App State function
Step 3: Monitor function

When saving this test case, select the test case type as Monitoring.
Add this test case to a test suite
Run the test suite like a usual test suite.
