.. _ondevice-context-menu:

Recording user actions
======================


.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline


When you hover your mouse pointer over the app that you are testing, you will notice a rectangular placeholder overlaid on top of various objects on the screen. You can also find the name of the highlighted object on the header. 

When a particular object is highlighted using the placeholder, it is selected and you can record various actions related to that object.

Left-clicking on a highlighted element opens up a context menu which lets you do the following:-

**1. Record user actions**

  Depending on the element highlighted, you can select one of the following actions to be recorded:

  :bolditalic:`Type           -` this records a 'Type' action on the object and is used to enter text into the selected element

  RobusTest provides you a number of options for :ref:`typing-text`  

  :bolditalic:`Tap            -` this records a 'Tap' action on the object that you have selected 

  :bolditalic:`Double Tap.    -` this records a 'Double Tap' action on the object that you have selected 

  :bolditalic:`Press and Hold -` this records a 'Press and Hold' or a 'Long Press' action on the object that you have selected 

  :bolditalic:`Zoom.          -` this records a 'Zoom' action on the object that you have selected

  :bolditalic:`Pinch.         -` this records a 'Pinch' action on the object that you have selected

  :bolditalic:`Swipe          -` this records a 'Swipe' action on the object that you have selected. For more details, go to the :ref:`swipe-on-page` section

  :bolditalic:`Swipe Till.    -` this records a 'Swipe Till' action on the object that you have selected

  :bolditalic:`Precise Tap    -` this records a 'Precise Tap' action on the object that you have selected

  Recording any of the above actions results in a corresponding test step being created

**2. Verify element**

  This option allows user to create a check or an assertion on an object. If the verification condition fails, the test step fails.

  You can know more on the :ref:`verification-main-page` page.

**3. Store element** 

  Sometimes you may want to store values corresponding to an element's attributes for later verification. These include attributes such as *'text'*, *'content-desc'*, *'checkable'*, *'checked'*, *'enabled'*, *'clickable'*, *'focused'*, *'selected'*, etc.

  You can use the 'Store Element' option to do so.

  **a.** Left-click on the element whose information you need to store and click on 'Store Element' on the Context Menu.

  **b.** You can see that a 'Store Element' test step has been recorded

  **c.** Expand this test step and go to the 'Return Data' tab. Here you can see all attribute information corresponding to the element selected. This information can be used for later verification ( as explained in the point above).

**4. Find concurrent element** 

  This option enables the user to identify and select the right element on which an action is to be performed.

  The elements on which an action is to be performed by the user are identified from the pagesource that is fetched for that app page.

  However, sometimes, it is found that an element is overlaid by one or more other elements in the pagsource. This results in the user not being able to highlight the correct element to record a user action.

  This is where the 'Find Concurrent Element' option comes into the picture and enables the user to idenitfy and select the right element. It does so as follows:

  **a.** Hover the mouse pointer over the area on the device screen where the element on which you wish to perform an action is present

  **b.** Left-click and select the 'Find Concurrent Element' option. 

    A 'Concurrent Elements' pop-up window now opens up. The 'Concurrent Elements' window lists all elements that are present on the area of the device screen on which you executed a left-click.

  **c.** On moving the mouse pointer over each element listed on the 'Concurrent Elements' window, the corresponding element is highlighted on the device screen.
  
  **d.** On the 'Concurrent Elements' window, click on the name of the element on which a user action is to be recorded and then click on the 'Save' button. This element is now selected and is seen highlighted on the device screen.
  
  **e.** Any user action that is now recorded by left-clicking on the highlighted element is executed on the highlighted element.

**5. Find parent element** 

  This option allows the user to identify the parent element of the highlighted element.

**6. Inspect element**

  This option allows the user to study the object and its attributes. This is useful for advanced users and for debugging.
