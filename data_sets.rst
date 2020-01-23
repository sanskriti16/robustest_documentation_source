.. _data-sets:

=========
Data Sets
=========

* To create a data set, you need to invoke the following API

HTTP Method: POST

URL: http://<RobusTest URL>/v3/dataset/new?accesskey=<access key>

Payload:

.. code-block:: JSON

  {
	"name" : "<Data Set Name>",
	"desc" : "<Data Set Description>",
	"project" : "<Project ID>",
	"headers" : ["<variable name 1>", "<variable name 2>"],
	"rows" : [{
		"device": "<device id optional>",
		"data" : {"<variable name 1>":"value", "<variable name 2>":"value"}
	},
	{
		"device": "<device id optional>",
		"data" : {"<variable name 1>":"value", "<variable name 2>":"value"}
	}]
  }

In the payload, provide the device id if you wish to run a specific data on a specific device. In case, you do not have such a requirement, you can leave the device values blank.

Sample

HTTP Method: POST

URL: http://devicelab.acme.com/v3/dataset/new?accesskey=d2342dsdad231313

Payload:

.. code-block:: JSON

  {
	"name" : "loginDataSet",
	"desc" : "Data Set for multiple user accounts",
	"project" : "d2312312dsadasdad",
	"headers" : ["username", "password"],
	"rows" : [{
		"device": "asda2113ssadad",
		"data" : {"username":"something@something.com", "password":"something123"}
	},
	{
		"device": "",
		"data" : {"username":"someone@someone.com", "password":"someone123"}
	}]
  } 

* Executing the above API will provide the DataSet in the response with the key _id.

* Update a Data Set

HTTP Method: PUT

URL:

.. code-block:: Java

	/v3/dataset/dataset_ID?accesskey=access_key

Payload

.. code-block:: JSON

  {
	"name" : "<Data Set Name>",
	"desc" : "<Data Set Description>",
	"project" : "<Project ID>",
	"headers" : ["<variable name 1>", "<variable name 2>"],
	"rows" : [{
		"device": "<device id optional>",
		"data" : {"<variable name 1>":"value", "<variable name 2>":"value"}
	},
	{
		"device": "<device id optional>",
		"data" : {"<variable name 1>":"value", "<variable name 2>":"value"}
	}]
  }

* Delete a Data Set

HTTP Method: DELETE

URL:

.. code-block:: Java

	/v3/dataset/dataset_ID?accesskey=access_key

* Get list of all data sets for a project

HTTP Method: GET

URL:

.. code-block:: Java

	/v3/datasets/project/:projectID?accesskey=access_key