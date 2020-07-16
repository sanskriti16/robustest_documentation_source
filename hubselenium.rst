.. _hub-selenium:

Selenium
========

.. image:: _static/buildURL.png	

1. create a web project
2. Hub url - point to nerve server 
3. Desired capabilities will look as below

desiredCapabilities={
"browserName":"[Browser Name]",
"accessKey" : "[User Access Key]",
"project": "[Project ID]"
}

4. Get browser status


URL:

http://[DEVICE LAB URL]/grid/browsers

HTTP Method: GET

