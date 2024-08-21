## Course 02: Calculator
______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the `H:\` drive!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______


### Tasks
1. Create a new java project without build tools like in [Course 01, Task 2](#task-2---basic-java-app)
2. Copy the code of `App.java` of [Course 01, Task 2](#task-2---basic-java-app) into your new `App.java`
3. (OPTIONAL) Additionally, add the following `static` methods inside `App`
   1. multiplizieren
   2. sin(x)
   3. x^y
4. Display a menu to the terminal which displays one option for each of your methods. For example:
    ``````
    CALCULATOR - please select:
    0: Programmende
    1: addieren
    2: dividieren
    3: multiplizieren
    4: sin(x)
    5: x^y
    ``````
5. Read in user input in the terminal
6. Display what parameters should now be provided by the user
7. Read in user input for each parameter the selected methods requires  (if you improved the parameters in `addieren` to `int... zahlen` you need to define a "stop" character like `s` for stop)
8. Run the selected method and display the result in the terminal
9. Repeat the programm until the user presses 0, which should close all open resources and exit the program.
