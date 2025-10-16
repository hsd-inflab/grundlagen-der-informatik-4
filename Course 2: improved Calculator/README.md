## Course 02: Calculator + Password Manager
______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the network drive (Dieser PC-> Netzwerkadressen)!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______

### Task overview
1. Improve the Calculator from Course 1
2. Implement a password manager

### Task 1: Improved Calculator
1. Create a new java project named `git4c2a` without build tools like in **Course 1, Task 1** 
2. Copy the code of `App.java` of **Course 1, Task 1** into your new `App.java`
3. all requirements and constraints from course 1 apply as well, regarding naming conventions etc.
4. To improve your calculators functionality, implement the following methods:
   1. sin(x)
   2. x^y
   3. gcd(), greatest common divisor (größter gemeinsamer Teiler) of two numbers
   4. fibonacci(n), which returns the nth Fibonacci number
   
   both 3 and 4 shall be implemented using recursion.

5. Update your menu method to support the added functionalities  
6. Commment your code where necessary. Good comments add context to code without explaining obvious things. A good rule of thumb is to explain ***WHY*** you do something and not **what** you are doing.


### Task 2: Password Manager
______

**ATTENTION:** Please **do not** use any of your actual passwords for this excercise, as they can be seen in plain text and may be saved in plain text on the computer.

Think of new, unique passwords that you never used and never will use.
______



1. Create a new java project named `git4c2b` without build tools. You may repurpose and adapt your CLI menu from the previous task. Implement the following functionalities:
     1. change password
     2. check password
     2. leave password manager
2. The following contraints apply:
     1. The default password is "123456".
     2. when setting a new password, it needs to contain at least:
          1. 8 characters in total
          2. One number
          3. One special character (* , - , /, ...)
          4. One uppercase character
     3. when changing the password, the new password must differ from the old one
     4. if the password change is permitted, the user must confirm the new password by entering it again.
     5. the password object (a string) must be properly encapsulated by the correct access modifiers and getter/setter functions.

    The full documentation for String Class can be found [here](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)

3. **OPTIONAL**: To improve password storage security, upgrade your program by using a hashcode for storing the password instead of plain text.     
    


