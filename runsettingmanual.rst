
.. _run-settings-manual:

Manual Run Setting
==================

.. role:: bolditalic
  :class: bolditalic

.. role:: underline
  :class: underline


Manual Run Setting is used when starting a new Manual Test Session

A Manual Run Setting consists of two kinds of settings: 

| **1. General Settings**
| **2. Performance Settings**

**1. General Settings**

By default, the 'General Settings' section has the following parameters and values:

   **a.** :bolditalic:`reset` 
     * default value: :bolditalic:`no` 
     * ensures that the app is not reset    

   **b.** :bolditalic:`uninstallAppAfterRun` 
     * default value: :bolditalic:`yes` 
     * this ensures that the app is uninstalled from the device at the end of the test session

   **c.** :bolditalic:`uninstallAppBeforeRun` 
     * default value: :bolditalic:`yes` 
     * this ensures that the app, if already installed, is uninstalled from the device at the beginning of a new test session

You can add/modify/delete other parameters to your run setting

**2. Performance Settings**

This section determines whether the performance metrics of an app needs to be captured or not

   **a.** :bolditalic:`monitor` 
     * default value: :bolditalic:`false` 
     * if *true*, enables the monitoring of various performance parameters such as Memory, CPU, Network Activity, etc.