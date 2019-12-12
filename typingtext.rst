.. _typing-text:

Typing text
===========

In order to enter text into a text field you need to do as follows:

1. Hover the mouse over the text field until that element is highlighted.

   * In case you are not sure that the right elemdnt is being highlighted, use the 'Find Concurrent Elements' option to identify the right element.

2. Perform a left-click action while the element is highlighted.

3. On the menu that opens up, click on the option 'Type'. An '*Enter Text*' window now pops up.

4. On the '*Enter Text*' window, you can do the following:

   a. Type the text value you would like to enter into the 'Input Text' field.

   .. image:: _static/entertext1.png

   b. Select the method by which you would lke to enter text from the drop down named 'Enter text using'.

      RobusTest provides you multiple methods of entering text into a text field. Let's have a look at these methods:

      1. Entering text using *RobusTest* - This is the default method by which text is entered. It is a custom method built by the RobusTest team.

      2. Entering text using the *Automation framework* - This method enables you to enter text using the functions available in the underlying Automation framework. E.g. using the method available on the Appium framework to enter text.

      3. Entering text using *Android Device Bridge*  - This method uses ADB to enter text into the text field,

   .. image:: _static/entertext2.png

   c. Choose whether to hide the device keyboard or not by selecting/unselecting the checkbox named '*Hide keyboard after entering text*'.

   .. image:: _static/entertext3.png

5. Click on the '*Save*' button. 

The input text will now be entered into the input field. 