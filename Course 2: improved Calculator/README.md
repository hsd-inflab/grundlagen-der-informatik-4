## Course 02: Calculator + Password Manager
______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the `H:\` drive!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______

### Task overview
1. Improve the Calculator from Course 1
2. Implement a password manager

### Task 1: Improved Calculator
1. Create a new java project without build tools like in **Course 1, Task 1**
2. Copy the code of `App.java` of **Course 1, Task 1** into your new `App.java`
3. all requirements and constraints from course 1 apply as well, regarding naming conventions, sanitizing inputs etc.
4. To improve your calculators functionality, implement the following methods:
   1. sin(x)
   2. x^y
   3. gcd(), greatest common divisor (größter gemeinsamer Teiler) of two numbers
   4. fibonacci(n), which returns the nth Fibonacci number
   both 3 and 4 shall be implemented using recursion.

5. Update your menu method to support the added functionalities

### Task 2: Password Manager
______

**ATTENTION:** Please **do not** use any of your actual passwords for this excercise, as they can be seen in plain text and may be saved in plain text on the computer.

Think of 
______



1. Add another menu point for a password manager. This action shall open another submenu with the following functionalities:
     1. set password
     2. change password
     3. check password
     4. leave password manager (return to calculator menu)
2. The following contraints apply:
     1. The default password is "123456". it has to be changed after the first call of the program.
     2. when setting a new password, it needs to contain at least:
          1. One uppercase letter
          2. One number
          3. One special character (* , - , /, ...)
          4. 8 characters in total
     3. when changing the password, the new password must differ from the old one
     4. the password object (a string) must be properly encapsulated by the correct access modifiers and getter/setter functions.
3. To improve password storage security, upgrade your program by using a hashcode for storing the password insteand of plain text.     
    
