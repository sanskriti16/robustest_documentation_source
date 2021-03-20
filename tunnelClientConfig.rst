.. _adding-new-devices-android:

Setting Up Tunneling
====================


.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline


In our context, tunneling is referred to the case when all requests from your test device go through a system/server of your choice. To set up tunneling, you need to do the following

1. Ensure that the IP address field for your device in Admin Console, is set. In case of Android devices, the IP address value is automatically set in the Admin Console and does not need manual updation. In case of iOS devices, the system cannot retrieve the IP address from the device and therefore this value needs to be manually set in the Admin Console.

2. Set the proxy on the mobile device on which you to run your tests

For iPhone, follow the steps below to set the proxy

i. Open up Settings > Wifi
ii. Click on the blue arrow next to your wifi connection.
iii. Scroll to the bottom where there is a section for HTTP Proxy.
iv. Select Auto from this section.
v. In the URL field enter the value 

http://{Device_Lab_URL}/tunnelConf

2. On the machine from which you want all requests to pass through, run the tunnel client using the following command

tunnel connect --tunnelKey <unique key for this instance> --deviceLabURL {Device_Lab_URL} --accessKey {User Access Key}

Make sure you store the tunnelKey used. This key needs to be passed on when running your tests

3. If running Appium tests, pass the value of the tunnelKey as a desired capability with the name "robustest.tunnelKey"
