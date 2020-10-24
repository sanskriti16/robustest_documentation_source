.. _hub-appium_organize:

Organize Appium Sessions Into Test Cases
========================================

*Grouping multiple Appium sessions into a single job*

When you run an Appium test job, the job may comprise many Appium sessions. For easier reporting and management, it is possible to group all the Appium sessions created as part of a job. Use the same value for  **robustestJobIdentifier** desired capability for Appium sessions belonging to the same job. Any appium session with the same value for robustestJobIdentifier, will be grouped together.

*Naming your Appium sessions*

Many automation frameworks are designed in such a way that they create a new Appium session for every test case. To be able to read such reports easily in RobusTest, user can use the **robustestSessionIdentifier**. This desired capability is meant to be unique for every Appium session within a job.

**Retrieving RobusTest Test Session ID**

Once your Appium tests starts, you can access details about your Appium session using the unique RobusTest Session ID. This ID is created when user tries to start an Appium session on RobusTest. RobusTest Session ID can we accessed in two ways

1. **robustestSessionIdentifier** - To retrieve the RobusTest session ID using the **robustestSessionIdentifier**, use the following API

**GET /v3/hub/sessionIdentifer/{robustestSessionIdentifer}**

The advantage of using the **robustestSessionIdentifier** to retrieve the RobusTest session ID is that even if the Appium session does not get created, the RobusTest session ID will help in accessing the appium log and other details. As mentioned earlier, the **robustestSessionIdentifier** will have to be passed as a desired capability.

2. **Appium Session ID** - To retrieve the RobusTest session ID using the Appium session ID use the following API

**GET /v3/hub/session/{Appium Session ID}**

When using this method, user can get the RobusTest Session ID only when you have a valid Appium session ID.