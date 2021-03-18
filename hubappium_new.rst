.. _hub-appium_new:

Run Appium Tests
================

.. toctree::
   :maxdepth: 2
   :hidden:


.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline

To run your Appium tests using the new RobusTest Hub for Appium, you need to do the following:

**1. Appium server URL** 

All RobusTest specific desired capabilities should be provided by appending 'robustest.' to the desired capability name e.g. **robustest.accessKey**. The default attributes provided by Appium should be used as it is.

* Use the RobusTest Hub URL for your Appium server URL.

- This will be of the form **http(s)://[RobusTest Device Lab URL]/wd/hub**

**2. Desired Capabilities**

**robustest.deviceID** - Provide the device details using the **robustest.deviceID** desired capability. 
*This is not mandatory in case of running mobile web tests as the system will automatically pick up a device based on desired capabilities mentioned. If you do provide deviceID for your mobile web tests, then the system will try to allocate the specific device requested for and fail if the device is not available*

* **robustest.projectID** - The RobusTest project under which you wish to run your tests should be provided using the *robustest.projectID* desired capability.

- **robustest.accessKey** - The user is authenticated using the RobusTest Access Key, provided using the *robustest.accessKey* desired capability.

* **platformName** - Depending on whether you wish to run your tests on Android or iOS, please select the appropriate platform name, provided using the *platformName* desired capability.

* **app** - In case you are running your tests on a mobile app, you also need to provide the *app* desired capability. This can be a local file or a remote file.

- **robustest.buildID** - If you are running your tests on a build uploaded to RobusTest and want to see the build details in your report, pass the *robustest.buildID* desired capability. The buildID is the unique identifier for a build that is uploaded to RobusTest.

* **browserName** - In case you are running your tests on a mobile browser, provide the *browserName* desired capability.

- **adbExecTimeout** - In case you are running your tests on a mobile browser, it is highly recommended to add the *adbExecTimeout* desired capability and give it a high value of say 2000000. This ensures that tests do not error due to timeout.

- *robustest.testcaseName* - To create a test case from an appium test session, you need to direct the system to do so. This can be done in two ways. Either by giving the desired capability as mentioned here or by making an API based request to the device lab. Details for the API are available at http://api.robustest.com/#tag/appium/paths/~1v3~1appium~1{appium_session_id}~1testcase/post


**3. Setting Timeout Values**

* **robustest.runSetting** - User can create a Run Setting and provide the Run Setting ID as the value of the *robustest.runSetting* desired capability to configure various aspects of the Appium job. The attributes currently supported are:

  - *runTimeout* - this value (in secs) can be used to specify the max amount of time a job can run before it is closed by the system on account of exceeding the value set for runTimeout.

  * *idleTimeout* - this value (in secs) can be used to specify the amount of time a job can be idle before the job can be closed by the system

  - *testcaseTimeout* - this value (in secs) can be used to specify the maximum run time of a test case. This value will be used by the system only when Advanced Integration with RobusTest Appium Hub is done.

4. Additional custom desired capabilities

a. **robustest.fallbackScreenshotMode** - this desired capability is specific to iOS test sessions. To ensure a higher success rate of screenshtos, user can use the *robustest.fallbackScreenshotMode* desired capability. Valid values are i. idevicescreenshot ii. appium. If this desired capability is not used, fallback method will not be employed to take a screenshot in case the default screnenshot method does not work.