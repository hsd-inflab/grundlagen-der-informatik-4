## Course 1: Calculator CLI

______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the `H:\` drive!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______

<details>
<summary> MacOS Users only - CLICK TO EXPAND </summary>

Please make sure to follow these steps to "downgrade" your TextEdit to save simple java files:

- on the menu bar on the top left corner of your screen, click on TextEdit, then Preferences.
- In the New Document tab, change the document format to Plain Text under the Format section. Uncheck the Smart quotes box under the Options section towards the bottom of the preference window.
- Switch to the Open and Save tab. Change the Opening files and Saving files to Unicode (UTF-8).
- Close the TextEdit application and re-open it. Open a new document.

</details>

### Task overview

1. Create, compile and run a simple "Hello World" java application with only a text editor and the command line.
2. Create and run a simple Java App, utilizing functions (methods) and recursion with VsCode.

### Tasks

#### Task 1 - Simple "Hello-Java-App"

1. Let your file explorer show file extensions to safe files with the correct `.java` file extension:

![](../images/windoof.png)

2. Open a simple text editor (Windows Notepad, Ubuntu Gedit or MacOs TextEdit) enter the following code and save it as ```Hello.java``` to your desired location:
    ```java
    public class Hello {
        public static void main(String args[]) {
            System.out.println("Hello Java");
        }
    }
    ```
3. Open a command line interface (Windows: `Powershell` or `Terminal` - *NOT* `cmd.exe`, Ubuntu: CTRL + SHIFT + T, MacOs: search for `Terminal`) and navigate to the location where you saved your Java Code with:

    ```bash
    cd PATH_TO_YOU_FILE
    ```

4. Type ```javac Hello.java``` and press enter
5. Now the java code has been compiled to ```Hello.class``` which you can run from within your terminal with:
    ```java
    java Hello
    ```

#### Task 2 - Basic Java App

*GENERAL NOTE*: While developing in VsCode, please check red squiggle lines and/or the "PROBLEMS" tab for any compilation errors or linter warnings. Often you can use the "Quick Fix" in the context menu (mouse over or `CTRL` + `.`, MacOs: `CMD` + `.`).

1. Create a new Java Project without build tools by...

    EITHER clicking on the "Create Java project" button in the explorer view of VsCode *(considering you have no directory currently opened, otherwise this button won't show up)*, selecting "No builds tools", choosing a directory to create the project in and naming it `se1c1`

    ![](../images/vscode_simple_java_app.gif)

    OR by opening the VsCode command palette (press CTRL+SHIFT+P, MacOS: CMD+SHIFT+P) and typing  *Java: Create Java Project*, selecting "No builds tools", choosing a directory to create the project in and naming it `se1c1`

    ![](../images/command_palette.png)

2. VsCode should have created the file `App.java` for you (if not, create it)
3. Change `App.java` to include
   1. a `main` Method (should be already inside)
   2. inside the `main` method declare the following variables and initialize them if a fitting value
      1. `eineZahl` of the type `int`
      2. `nochEineZahl` of the type `int`
      3. `eineKommaZahl` of the type `double`
      4. `eineZeichenKette` of the type `String`
   3. outside of the `main` method, but inside `App`
      1. a `static` method `addieren` with two parameters (also called "arguments") of the type `int`, for example `a` and `b`, that returns the addition of `a` and `b`
      2. a `static` method `dividieren` with two parameters of the type `double`, for example `a` and `b`, that returns `a` divided by `b`
      3. a `static` method `ggt` (größter, gemeinsamer Teiler) that calculates the greatest common divisor of the two `int` variables `a` and `b`
         1. constraint: use recursion
   4. call `addieren` with `a:eineZahl` and `b:nochEineZahl` and save the result in the variable `summe`
   5. call `dividieren` with `a:eineKommaZahl` and `b:summe` and save the result in the variable `quotient`
   6. Use the method `System.out.println` to print out `eineZeichenKette + quotient` to the integrated terminal in VsCode
   7. call `ggt` with `a:eineZahl` and `b:nochEineZahl` and use `System.out.println` to print the result to the terminal
   8. Explain why `addieren` and `dividieren` need to be declared as `static`
   9. (OPTIONAL) Change `addieren` the arguments to `int... zahlen`, declare and initialize the variable `int summme = 0` inside the method body of `addieren` and iterate of the provided arguments with a for-loop to add each argument to `summe` and finally return `summe` at the end
