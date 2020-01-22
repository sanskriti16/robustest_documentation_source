Mapping to Data Set
===================


To be able to provide your test cases with non-default data you need to do the following

1. Create a function

The step or set of steps that you wish to parameterize should be inside a function and your test cases should use the function. e.g. in case you are trying to paramterize the login steps, it would be a good idea to put the steps to enter username, password and submit the data inside a function. This also creates a logical entity which takes care of login process.

2. Parameterize the data

* Open the function test case for editing.

* Open the User Data tab for the test step that you are trying to parameterize.

* Click on the "Enable Parameterization" button for the field that you wish to parameterize.

* Provide a userfriendly variable name that identifies that field. Make sure there are no spaces in the name.

* Do the same for all the test steps that you wish to parameterize

* Save the function test case

3. Create a Data Set and note down the Data Set ID. (To know more about data sets, read :ref:`data-sets`)

4. Create a run specifying the data set to be used and how to use the data set`1

HTTP Method: POST

URL: http://<RobusTest URL>/v3/run/new?accesskey=<access key>

Payload:

.. code-block:: JSON

  {
  "testsuite": "<Test Suite ID>",
  "project": "<Project ID>",
  "build": "<Build ID>",
  "devices": [
    "<comma separated device IDs>"
  ],
  "settings": {
    "appium": {
      "automationName": "UiAutomator2",
      "disableAndroidWatchers": "true",
      "forceEspressoRebuild": "true",
      "fullReset": "true",
      "ignoreUnimportantViews": "true",
      "noReset": "false",
      "noSign": "true"
    },
    "general": {
      "checkElementIsVisible": "yes",
      "collectLog": "yes",
      "collectPerformance": "yes",
      "elementWaitTimeOut": "30",
      "enterTextMethod": "appium",
      "handleAndroidPermissionPopup": "allowAll",
      "pagesourceTimeout": 100,
      "recordingMode": "normal",
      "retryFailedTests": 0,
      "runOnlatestbuild": "true",
      "streamPagesource": "yes"
    },
    "notification": {}
  },
  "setting": "",
  "datasetID": "<Data Set ID>",
  "datasetMode": "<valid value is strict or blank>"
 }

If you set the datasetMode to strict, while running the tests, the dataset will be run only on the corresponding devices. In case the datasetMode is not set to strict, then the system randomly assigns the dataset to the devices on a first come first serve basis.

Sample

HTTP Method: POST

URL: http://devicelab.acme.com/v3/run/new?accesskey=d2342dsdad231313

Payload:

.. code-block:: JSON

  {
  "testsuite": "5e0d18075752875f4d723e01",
  "project": "5d6f3d1f57528725c1afa13b",
  "build": "5df1e691575287692822d4d9",
  "devices": [
    "5d6f3ef4c74f741abb97e23c","5ada4c74f741abb97e23c"
  ],
  "settings": {
    "appium": {
      "automationName": "UiAutomator2",
      "disableAndroidWatchers": "true",
      "forceEspressoRebuild": "true",
      "fullReset": "true",
      "ignoreUnimportantViews": "true",
      "noReset": "false",
      "noSign": "true"
    },
    "general": {
      "checkElementIsVisible": "yes",
      "collectLog": "yes",
      "collectPerformance": "yes",
      "elementWaitTimeOut": "30",
      "enterTextMethod": "appium",
      "handleAndroidPermissionPopup": "allowAll",
      "pagesourceTimeout": 100,
      "recordingMode": "normal",
      "retryFailedTests": 0,
      "runOnlatestbuild": "true",
      "streamPagesource": "yes"
    },
    "notification": {}
  },
  "setting": "",
  "datasetID": "5e135c765752875a2a64d33a",
  "datasetMode": "strict"
 }

