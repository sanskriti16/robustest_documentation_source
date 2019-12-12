.. _more-on-functions:

More about functions
====================

**1. Setup Functions**

While creating a function, the user has to choose an option from the 'Category' drop down to determine the type of function being created.

By default, this dropdown has the value 'None'. Functions created using this default value are your regular functions. They are created with the intention of utilising the re-usability aspect of a function.

The second category of functions are what are known as *Setup functions* They are a unique category of functions that RobusTest enables you to create.

Sometimes, there occurs scenarios in which: 

**a.** prior to a test case being executed, a series of actions need to be performed to set the test data bed and bring it to a specific state.
**b.** after a test case has been executed, a series of actions need to be performed to reset the test data bed or bring it to a required state.
**c.** both - points **a.** and **b.** above apply

Such scenarios are recorded as part of *Setup functions*.

* *Setup functions* are used for setting up or tearing down of the test bed before or after the actual test case is executed.

* *Setup functions* are not considered a part of the actual test case being executed.

* If a test step within a *Setup functon* fails, then, unlike a regular function, it does not result in the failure of the test case that calls the setup function.

**2. Functions within a function**

Another functionality that RobusTest provides is the ability to call one or more functions within a function. 

This capapbility allows you to create highly modular test cases that greatly helps to enhance the readability of your test cases as well as allows you to maintain and update your test cases more easily.

E.g. Let us say, you want to create a test case that allows a customer to select a specific billing plan and then pay for it.

This test case could include multiple functions to perform the following actions:

* Login to the app
* Enter Customer information
* Select a type of purchase
* Select a billing option
* Execute a payment

Each of the above steps in our example is a function. Each of these functions could themselves constitute of one or more functions.

E.g. the function '*Enter Customer Information*' above may constitute of the following functions:

* Enter customer Personal details
* Enter customer Billing address
* Enter customer Shipping address

Designing test cases in the above manner allows you to easily understand the scenario being tested and provides you more control when maintaining and updating test cases.

**3. Functions and Parametrisation**

