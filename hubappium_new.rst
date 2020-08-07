.. _hub-appium_new:

Appium Hub 2.0
==============


 .. image:: _static/buildURL.png

**Configuration**

With the refreshed version of RobusTest Hub for Appium, you get a cleaner way of running your Appium tests on apps as well as browsers

To run your Appium tests using the new RobusTest Hub for Appium, you need to do the following

1. Provide the RobusTest Hub URL:

This will be of the form 

**http(s)://[RobusTest Device Lab URL]/wd/hub**

Note that this is different from the older Hub which used to run on port 3142 by default

2. Provide the project ID:

The RobusTest project under which you wish to run your tests should be provided using the **projectID** desired capability.

3. Provide the Access Key

The user is authenticated using the RobusTest Access Key, provided using the **accessKey** desired capability.

4. Provide the platform name

Depending on whether you wish to run your tests on Android or iOS, please select the appropriate platform name, provided using the **platformName** desired capability.

5. Provide the Device

Provide the device details using the **deviceID** desired capability. 
*This is not mandatory in case of running mobile web tests as the system will automatically pick up a device based on desired capabilities mentioned*.

**Running tests on Mobile App**

In addition to the above desired capabilities, you also need to provide the *app* desired capability

**Running tests on mobile browser**

In addition to the above desired capabilities, you also need to provide the **browserName** desired capability.

It is highly recommended to also add the **adbExecTimeout** desired capability and give it a high value of say 2000000. This ensures that tests do not timeout.

**Grouping multiple Appium test sessions into a single job**

When you run an Appium job on the RobusTest Hub, it may contain many Appium sessions. Fo you to group all of these sessions together, as part of a singel test run or a job, you can use the **robustestJobIdentifier** desired capability. Any appium session with the same value for robustestJobIdentifier, will be grouped together. Therefore, it is important to use it properly.

**Getting the RobusTest test session ID**

Once you start your Appium tests, you will want to see details about your Appium session. Details of your Appium session can be retrieved using the RobusTest Session ID which gets created when you try to start an Appium session on RobusTest. You can get the RobusTest Session ID in two ways

1. By specifying a unique identifier **robustestSessionIdentifier** with your test session - The advantage of using this identifier to get the RobusTest session ID is that, even if your Appium session does not get created due to various reasons, you will have the RobusTest session ID which will help you access the appium log and other details. The identifier will have to passed as a desired capability when starting your Appium session.

To retrieve the RobusTest session ID using the **robustestSessionIdentifier**, use the following API

**GET /v3/hub/sessionIdentifer/{robustestSessionIdentifer}**

2. By using the Appium session ID that is created when an Appium session starts. When using this method, you will be able to get the RobusTest Session ID only when you have a valid Appium session ID.

To retrieve the RobusTest session ID using the **robustestSessionIdentifier** use the following API

**GET /v3/hub/session/{Appium Session ID}**

