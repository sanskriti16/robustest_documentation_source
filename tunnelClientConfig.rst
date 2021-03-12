.. _adding-new-devices-android:

Setting Up Tunneling
====================


.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline


To configure tunneling for your tests in such a way that all requests from your test device go through a system/server that you have identified, you need to do the following

1. Set the proxy on the mobile device on which you to run your tests

For iPhone, follow the steps below to set the proxy

i. Open up Settings > Wifi
ii. Click on the blue arrow next to your wifi connection.
iii. Scroll to the bottom where there is a section for HTTP Proxy.
iv. Select Auto from this section.
v. In the URL field enter the value 

http://{RobusTest_URL}/tunnelConfiguration

2. On the machine from which you want all requests to pass through, run the following command

<tunnel binary> connect --key <key unique to the client> --nerve {RobusTest_URL} --accessKey {User Access Key}

Make sure you note down the unique key, this key will need to be passed on when running your tests

3. If running Appium tests, pass the value of the unique key as robustest.tunnelKey
