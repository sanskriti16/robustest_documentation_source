.. _invert-verification:

Invert Verification
===================

Another interesting feature available on RobusTest is to invert the results of a verification action.

Usually, if a condition mentioned in a verification test step is a match, the test step passes on execution.

If 'Invert Verification' is enabled for the same test step, the result of the comparison is inverted, i.e., the test step will fail in execution

This option can be of help in many use cases.

**E.g.1:** Let us say that a music player is visible on an app (see example from :ref:`verify-element-exists` section) 

Our goal is to ensure that the music player is closed (i.e. no longer visible on the page) after the 'Close' button is clicked on.

We can do this using the 'Invert Verification' option as follows:

1. Open the music player
2. Left-click on the music player element and click on 'Verify Element'\n
   **Note:** If the 'Save' button is clicked at this point, the verification test step recorded checks if this specific element is availabe on the page or not

3. Enable 'Invert Verificaiton' by clicking on the check box
4. Click on the 'Save' button