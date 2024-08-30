## Course 1: Calculator CLI

______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the `H:\` drive!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______
<!---
<details>
<summary> MacOS Users only - CLICK TO EXPAND </summary>

Please make sure to follow these steps to "downgrade" your TextEdit to save simple java files:

- on the menu bar on the top left corner of your screen, click on TextEdit, then Preferences.
- In the New Document tab, change the document format to Plain Text under the Format section. Uncheck the Smart quotes box under the Options section towards the bottom of the preference window.
- Switch to the Open and Save tab. Change the Opening files and Saving files to Unicode (UTF-8).
- Close the TextEdit application and re-open it. Open a new document.

</details>
--->
### Task overview

1. Create a simple Command Line Interface Calculator.
2. Compile and run the program you created. 


### Tasks

#### Task 1 - Basic Java Calculator App

*GENERAL NOTE*: While developing in VsCode, please check red squiggle lines and/or the "PROBLEMS" tab for any compilation errors or linter warnings. Often you can use the "Quick Fix" in the context menu (mouse over or `CTRL` + `.`, MacOs: `CMD` + `.`).

1. Create a new Java Project without build tools by...

    EITHER clicking on the "Create Java project" button in the explorer view of VsCode *(considering you have no directory currently opened, otherwise this button won't show up)*, selecting "No builds tools", choosing a directory to create the project in and naming it `git4c1`

    ![](../images/vscode_simple_java_app.gif)

    OR by opening the VsCode command palette (press CTRL+SHIFT+P, MacOS: CMD+SHIFT+P) and typing  *Java: Create Java Project*, selecting "No builds tools", choosing a directory to create the project in and naming it `git4c1`

    ![](../images/command_palette.png)


2. VsCode should have created the file `App.java` for you (if not, create it)
3. In `App.java`, implement the following functionalities for the basic calculator:
   1. a `main` Method (should be already inside)
   2. A method each for the four basic arithmetic operations (Addition, Subtraction, Multiplication, Division)
      These methods have to fit the following requirements:
      1. A meaningful name 
      2. Two input parameters with appropriate data types
      3. An appropriate return type
      4. The name of the method as well as input parameter shall follow the naming conventions stated in the lecture
      5. A static modifier
   
      example:
        ```java
        public class App {
            public static void main(String args[]) {
                /*...*/
         
            }
            /*....*/
            public static double subtract(double minuend, double subtrahend){
                /*..*/
            }   
            /*....*/  
        }
        ```

       inspiration for proper naming of parameters (in english) can be found [here](https://en.wikipedia.org/wiki/Template:Arithmetic_operations)
        
   3. A method that implements a menu displayed on the terminal with the following requirements:
      1. Display menu for all implemented methods
        
            example:
            ``````
            CALCULATOR - please select:
            0: end program
            1: add
            2: subtract
            ..
            ...
            ....
            ``````
      2. Read in user input from terminal
      3. Display what parameters should now be provided by the user
      4. Read in user input for each parameter the selected methods requires
      5. Run the selected method and display the result in the terminal
      6. Repeat the programm until the user presses 0, which should close all open resources and exit the program.

   4. Explain why the methods need to be declared as `static`.
            
   <!--5. Make sure to sanitize the user inputs. The programm shall not crash or throw an exception when user inputs do not match the desired data type! -->
#### Task 2 - Use the CLI Calculator
<!-- Let your file explorer show file extensions to save files with the correct `.java` file extension:    (this is optional)

![](../images/windoof.png)
-->
1. Open a command line interface (Windows: `Powershell` or `Terminal` - *NOT* `cmd.exe`, Ubuntu: CTRL + SHIFT + T, MacOs: search for `Terminal`) and navigate to the location where you saved your Java Code with:

    ```bash
    cd PATH_TO_YOU_FILE
    ```
    You can obtain `PATH_TO_YOUR_FILE` in vscode by right-clicking on the folder where App.java is saved (should be called `src`) and choosing Copy Path (or SHIFT + ALT + C).

2. Type ```javac App.java``` and press enter
   
3. Now the java code has been compiled to ```App.class``` which you can run from within your terminal with:
    ```java
    java App
    ```

4. Explain what happened during steps 2 and 3.

5. Test your code with different inputs. If it crashes, adapt your code from Task 1.

