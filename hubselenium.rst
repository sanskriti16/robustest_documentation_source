.. _hub-selenium:

Run Selenium Tests
==================

.. image:: _static/buildURL.png	

1. create a web project
2. Hub url - point to nerve server 
3. Desired capabilities will look as below

::

	{
	  "browserName":"[Browser Name]",
	  "accessKey" : "[User Access Key]",
	  "projectID": "[Project ID]"
	}

4. Get browser status

HTTP Method: GET

URL: http://[DEVICE LAB URL]/grid/browsers

