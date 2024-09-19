# JavaExceptions
 _(derived from CISC191Exceptions)_


Java Test Driven Development (TDD) project to program Java classes with unit testing ( with **JUnit** )
________

<details>
 <summary><em>source</em></summary>


 ![220px-MesaLogo](https://github.com/schougaard/SanDiegoMesaCISC191ProgrammingChallenges/assets/716243/334f6724-6afa-4198-9eff-7c49c472cd35)

# San Diego Mesa College CISC 191 Programming Challenges
Programming challenges for San Diego Community College CISC 191 Intermediate Java classes.

Created by
- Professor Dr. Tasha Frankie
- and Professor [Allan Schougaard](https://github.com/schougaard), San Diego Mesa College.

With contributions from: 
- Dom David,
- [Dan Sullivan](https://github.com/uid100)
________

</details>
<details>
 <summary>Overview</summary>

Assignment Overview

Java defines special types of errors called exceptions for a number of reasons:

 - To separate error handling from program logic. Exceptions allow programmers to write their code in a more modular and reusable way, by separating the code that detects and handles errors from the code that performs the main logic of the program. This makes the code easier to read, understand, and maintain.
 - To provide a robust and consistent way to handle errors. Exceptions provide a standard way to handle errors, which makes Java code more predictable and reliable. This is especially important in large and complex applications, where errors can occur in many different places.
 - To propagate errors up the call stack. Exceptions can be propagated up the call stack, which allows errors to be handled at the appropriate level. For example, if a method throws an exception, the calling method can catch the exception and handle it accordingly. This allows programmers to centralize error handling in certain parts of the application, making it easier to manage and troubleshoot errors.
 - To provide information about errors. Exceptions contain information about the error, such as the type of error, the stack trace, and any additional details. This information can be used to log the error, display a meaningful error message to the user, or take other corrective action.

Java defines two types of exceptions: checked exceptions and unchecked exceptions. Checked exceptions are exceptions that must be explicitly handled by the programmer. Unchecked exceptions are exceptions that do not need to be explicitly handled by the programmer.

Checked exceptions are typically used to handle errors that are beyond the control of the programmer, such as errors caused by the underlying operating system or hardware. Unchecked exceptions are typically used to handle errors that are caused by programmer mistakes, such as null pointer exceptions and array index out of bounds exceptions.

Overall, exceptions are a powerful tool that can be used to improve the robustness, reliability, and maintainability of Java code.

Here are some specific examples of how exceptions can be used in Java:

 - Handling errors caused by user input. If a user enters invalid input, the program can throw an exception, which can then be handled to display a meaningful error message to the user and allow them to try again.
 - Handling errors caused by file operations. If a program tries to open a file that does not exist, the program can throw an exception, which can then be handled to notify the user of the error and allow them to take corrective action.
 - Handling errors caused by network operations. If a program tries to connect to a network server that is unavailable, the program can throw an exception, which can then be handled to retry the connection or notify the user of the error.

By using exceptions to handle errors, Java programs can become more robust, reliable, and user-friendly.
________

</details>
<details>
 <summary>Instructions</summary>

## _(Open the Project)_
1. From the **<> Code** dropdown link in the repository (above), download the Zip file to your computer.
2. Extract the files to your working folder
3. Open Eclipse and import the project. 
   - You can use File>Import menu item or right-click in the Package Manager and choose Import.
   - select General>Projects from Folder or Archive
   - navigate into the project until you see the `bin` and `src` folders, and choose *open*
4. Expand the project in the package explorer and find the .java files below the **src** folder.

## _(Complete the Assignment)_

</details>
<details>
 <summary>Code Layout</summary>
 
You will be completing code that deals with banking and bills. In the past, we may have handled input validation a little differently with simple if-statements and early returns of specific values. This time, you will handle special behaviors dealing with values using Exceptions.
___________

</details>
<details>
 <summary>Programming Tasks</summary>

 
## Programming Task(s)

### CheckoutBill
When you run the tester file you will see that the first failure is when the code expects an Exception to be thrown. 

_Be careful about accidentally running the CheckoutBill class since it has a main method. You may not realize that you are not running the tester class._

1. The bill amount should be greater than 0. Throw an `IllegalArgumentException` if the parameter does not meet this requirement. Otherwise, set the instance variable accordingly.
In Java to throw an exception you add the following:
```
throw (new MyExceptionName());
```
You are creating an object that is an `Exception` type and throwing it.

The term *throwing an exception* in Java is used to describe the process of creating an exception object and passing it to the runtime system. The runtime system will then search for an exception handler in the call stack, starting with the current method and working its way up. If an exception handler is found, the exception will be handled and the program will continue to execute. If an exception handler is not found, the program will terminate. The term "throwing" is used to describe this process because it is analogous to throwing a ball. When you throw a ball, you are transferring control of the ball to the person who catches it. Similarly, when you throw an exception, you are transferring control of the exception to the runtime system. The runtime system is responsible for handling exceptions in a way that is appropriate for the application. For example, the runtime system may display an error message to the user, log the error, or terminate the application.

2. Uncomment the next tester method in the tester class. Fix the `setTipPercent()` method so that it throws an exception if the parameter does not meet the requirement.
3. Uncomment the next tester which will focus on the `calculateTotalBill()` method.
Fix the method so that it throws an `IllegaStateException` if the bill or tipPercent do not have proper values. The current setup allows the creation of a `CheckoutBill` object that initializes the instance variables to undesirable values. Do not alter this behavior as this is by design.
4. Uncomment the next tester method (`testMain()`).
Now you must handle exceptions in the main method of the CheckoutBill class. Note that you will not actually have to do much in the catch clause other than printing the error to the console.

To handle an exception in Java means to take corrective action when an error occurs. This can involve logging the error, displaying a meaningful error message to the user, or taking other steps to recover from the error and continue executing the program.

There are two main ways to handle exceptions in Java:
Using the try-catch-finally block. The try-catch-finally block is the most common way to handle exceptions in Java. It allows you to specify a block of code that is to be executed, and to catch any exceptions that occur within that block. The finally block is optional, but it is often used to perform cleanup tasks, such as closing resources.
Using the try-with-resources statement. The try-with-resources statement is a newer way to handle exceptions in Java. It is specifically designed for handling resources that must be closed after they are used. For example, you can use the try-with-resources statement to handle files, database connections, and network sockets.

try {
  // Code that may throw an exception
} catch (Exception e) {
  // Handle the exception here
} finally {
  // Perform cleanup tasks here
}
In this programming assignment, you are not accessing resources so you do not need the finally block. 
try{
  // code that may throw an exception
}catch( Exception e){
  //handle exception here or print the exception to the console
}
BankAccount
Exceptions are a class in Java. The BankAccount will now have you creating classes that subclass the Exception class.

Uncomment the next tester method which now uses the BankAccount class.
Deposit
a) This method asks you to throw a specific type of exception that does not exist. Create a class of the described exception that extends the Exception class.

b) Check to see if should throw the exception and throw it, otherwise, proceed with the method's logic.

A method that throws an exception must declare so in the header. Add throws InvalidAmountException at the end of the method signature so it looks like the line below. 
public void deposit(double amount) throws InvalidAmountException
Withdraw
a) Take a look at the comments of the method. Create the missing exception classes similar to the deposit method.

b) Throw the exceptions based on the behavior described in the comments. Don't forget to add the throws declaration in the method's header. Since this method throws more than one error, make it so that it throws a generic Exception so that it covers any subclass of Exception.

c) Handle the rest of the logic of the method.

InvalidAmountException
Uncomment the next tester method.
Add the missing constructor.
Now that you have a constructor with a parameter, wherever you use the non-parameterized constructor, you must add the amount. For example, BankAccount uses this exception a lot.
Add a getMessage method that returns a message similar to the one shown in the tester method. As usual, care of any required white spaces.
Attempt the remainder of the tester methods now. For the last section, explore subclassing RuntimeException instead of Exception. What's the difference between check and unchecked exceptions?
___________

</details>

## Complete and zip the project
1. Run and add the code to the src folder until the tests are successful.
2. Uncomment each test case in the **Test** file (`TestAdvancedClasses.java`), one at a time. 
Do not modify the content in this file except to uncomment the tests. Add and modify class files
as needed for the tests to pass.
3. Review and refactor any of the code as needed:
    - be sure your code follows good coding practices and coding style and standards.
    - update the javadoc comments at the top of the file to add your name as author
    - update the comments for each method in the file.
4. Export the project as a zip file and submit your work.

___________

## Rubric

[Rubric](Rubric.md)


___________

_this repository is a subset of the CISC191 exercises. It is derived from the CISC191ProgrammingChallenges 
activity hosted by Professor Allan Schougaard, San Diego Mesa College, and not a direct fork._

_This project is to decompose that repository into git submodules_
