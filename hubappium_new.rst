.. _hub-appium_new:

Run Appium Tests
================

.. toctree::
   :maxdepth: 2
   :hidden:

To run your Appium tests using the new RobusTest Hub for Appium, you need to do the following

1. Appium server URL - Use the RobusTest Hub URL for your Appium server URL:

This will be of the form 

**http(s)://[RobusTest Device Lab URL]/wd/hub**

2. Desired Capabilities

**projectID** - The RobusTest project under which you wish to run your tests should be provided using the **projectID** desired capability.

**accessKey** - The user is authenticated using the RobusTest Access Key, provided using the **accessKey** desired capability.

**platformName** - Depending on whether you wish to run your tests on Android or iOS, please select the appropriate platform name, provided using the **platformName** desired capability.

**deviceID** - Provide the device details using the **deviceID** desired capability. 
*This is not mandatory in case of running mobile web tests as the system will automatically pick up a device based on desired capabilities mentioned. If you do provide deviceID for your mobile web tests, then the system will try to allocate the specific device requested for and fail if the device is not available*

**app** - In case you are running your tests on a mobile app, you also need to provide the *app* desired capability

**buildID** - If you are running your tests on a build uploaded to RobusTest and want to see the build details in your report, pass the **buildID** desired capability. The buildID is the unique identifier for a build that is uploaded to RobusTest.

**browserName** - In case you are running your tests on a mobile browser, provide the **browserName** desired capability.

**adbExecTimeout** - In case you are running your tests on a mobile browser, it is highly recommended to add the **adbExecTimeout** desired capability and give it a high value of say 2000000. This ensures that tests do not error due to timeout.


3. Setting Timeout Values

**runSetting** - User can create a Run Setting and provide the Run Setting ID as the value of the **runSetting** desired capability to configure various aspects of the Appium job. The attributes currently supported are

a. *runTimeout* - this value (in secs) can be used to specify the max amount of time a job can run before it is closed by the system on account of exceeding the value set for runTimeout.

b. *idleTimeout* - this value (in secs) can be used to specify the amount of time a job can be idle before the job can be closed by the system

c. *testcaseTimeout* - this value (in secs) can be used to specify the maximum run time of a test case. This value will be used by the system only when Advanced Integration with RobusTest Appium Hub is done.