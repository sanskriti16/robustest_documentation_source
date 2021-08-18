Capturing device screen as video
================================

When running your automated tests, you may want to capture the screen of the mobile device. This helps in more accurate debugging in many cases.

RobusTest enables you to capture the mobile device screen as a video.

1. Currently you can capture device screen for Android devices

2. You can capture device screen for Espresso test runs

*Configuring your Espresso test runs to capture device screen*


1. The device screen video file will be pushed to an external storage source. Currently, screen recording files can be pushed to two storage providers - Google and AWS.

2. Start by creating a storage integration

3. Once created note the integration ID

4. In the Run Settings that you shall use for your automation job, specify the details under testDataCollections to inform the system that your test requires that device screen is captured. This should be done in the following way

4a. Specify stats

4b. Specicy video