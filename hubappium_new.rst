.. _hub-appium_new:

Run Appium Tests
================

.. toctree::
   :maxdepth: 2
   :hidden:
   
   hubappium_development

 .. image:: _static/buildURL.png

**Configuration**

With the refreshed version of RobusTest Hub for Appium, you get a cleaner way of running your Appium tests on mobile apps as well as mobile browsers

To run your Appium tests using the new RobusTest Hub for Appium, you need to do the following

1. Appium server URL - Use the RobusTest Hub URL for your Appium server URL:

This will be of the form 

**http(s)://[RobusTest Device Lab URL]/wd/hub**

2. Desired Capabilities

**projectID** - The RobusTest project under which you wish to run your tests should be provided using the **projectID** desired capability.

**accessKey** - The user is authenticated using the RobusTest Access Key, provided using the **accessKey** desired capability.

**platformName** - Depending on whether you wish to run your tests on Android or iOS, please select the appropriate platform name, provided using the **platformName** desired capability.

**deviceID** - Provide the device details using the **deviceID** desired capability. 
*This is not mandatory in case of running mobile web tests as the system will automatically pick up a device based on desired capabilities mentioned*.

*app* - In case you are running your tests on a mobile app, you also need to provide the *app* desired capability

**buildID** - If you are running your tests on a build uploaded to RobusTest and want to see the build details in your report, pass the **buildID** desired capability. The buildID is the unique identifier for a build that is uploaded to RobusTest.

**browserName** - In case you are running your tests on a mobile browser, provide the **browserName** desired capability.

**adbExecTimeout** - In case you are running your tests on a mobile browser, it is highly recommended to add the **adbExecTimeout** desired capability and give it a high value of say 2000000. This ensures that tests do not error due to timeout.

**Configuring Appium test reports**

*Grouping multiple Appium test sessions into a single job*

When you run an Appium test job, the job may comprise many Appium sessions. For easier reporting and management, it is possible to group all the Appium sessions created as part of a job. Use the same value for  **robustestJobIdentifier** desired capability for Appium sessions belonging to the same job. Any appium session with the same value for robustestJobIdentifier, will be grouped together.

*Naming your Appium sessions*

Many automation frameworks are designed in such a way that they create a new Appium session for every test case. To be able to read such reports easily in RobusTest, user can use the **robustestSessionIdentifier**. This desired capability is meant to be unique for every Appium session within a job.

**Retrieving RobusTest Test Session ID**

Once your Appium tests starts, you can access details about your Appium session using the unique RobusTest Session ID. This ID is created when user tries to start an Appium session on RobusTest. RobusTest Session ID can we accessed in two ways

1. **robustestSessionIdentifier** - To retrieve the RobusTest session ID using the **robustestSessionIdentifier**, use the following API

**GET /v3/hub/sessionIdentifer/{robustestSessionIdentifer}**

The advantage of using the **robustestSessionIdentifier** to retrieve the RobusTest session ID is that even if the Appium session does not get created, the RobusTest session ID will help in accessing the appium log and other details. As mentioned earlier, the **robustestSessionIdentifier** will have to be passed as a desired capability.

2. Appium Session ID - To retrieve the RobusTest session ID using the **robustestSessionIdentifier** use the following API

**GET /v3/hub/session/{Appium Session ID}**

When using this method, user can get the RobusTest Session ID only when you have a valid Appium session ID.