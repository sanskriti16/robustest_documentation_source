.. _hub-appium_new:

Appium
======


 .. image:: _static/buildURL.png

**Configuration**

With the refreshed version of RobusTest Hub for Appium, you get a cleaner way of running your Appium tests on apps as well as browsers

To run your Appium tests using the new RobusTest Hub for Appium, you need to do the following

1. Provide the RobusTest Hub URL:

This will be of the form 

*http(s)://[RobusTest Device Lab URL]/wd/hub*

Note that this is different from the older Hub which used to run on port 3142 by default

2. Provide the project ID:

The RobusTest project under which you wish to run your tests should be provided using the **projectID** desired capability.

3. Provide the Access Key

The user is authenticated using the RobusTest Access Key, provided using the **accesskey** desired capability.

4. Provide the platform name

Depending on whether you wish to run your tests on Android or iOS, please select the appropriate platform name, provided using the **platformName** desired capability.

5. Provide the Device

Provide the device details using the **deviceID** desired capability. This is not mandatory in case of running mobile web tests as the system will automatically pick up a device based on desired capabilities mentioned.

**Running tests on Mobile App**

In addition to the above desired capabilities, you also need to provide the *app* desired capability

**Running tests on mobile browser**

In addition to the above desired capabilities, you also need to provide the **browserName** desired capability.

It is highly recommended to also add the **adbExecTimeout** desired capability and give it a high value of say 2000000. This ensures that tests do not timeout.

**Gouping all Appium test sessions fom a single job**

When you run an Appium job on the RobusTest Hub, it may contain many Appium sessions. Fo you to mark all of the 

**Getting the obusTest session ID**

Once you stat you Appium tests, you will want to see details about you test un
You can get the RobusTest Session ID in twwo ways

1. Using your 
