## Course 4: JavaFX
______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the `H:\` drive!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______


### Topic

A calculator app made with JavaFX.

### Tasks

1. Create the Maven project ```se1c4``` by using the archetype `javafx-archetype-simple` from `org.openjfx` to create a **JAVA FX** (not Swing!) appliction

    ![](../images/vscode_maven_java_app.gif)

    **IMPORTANT:** if you have Java 21 installed instead of Java 17 (you can check the version with `java --version` in the terminal),
   you need to set the javafx-controls dependency version to 20 inside pom.xml!

3. add the following dependency to your `pom.xml` file:
   
    ```xml
    <dependency>
        <groupId>net.objecthunter</groupId>
        <artifactId>exp4j</artifactId>
        <version>0.4.8</version>
    </dependency>
    ```
4. Add the following line to your `module-info.java`

    ```
    requires exp4j;
    ```
    
5. The warning...

    *Name of automatic module `exp4j` is unstable, it is derived from the module's file name.*
  
   ...can be IGNORED (the package creator did not follow java module naming conventions)!

6. ***IMPORTANT for Apple💻🍎 Mac M1/M2/M3 (not Intel!) users at home...***

   Change the javafx-controls dependency, to include

   `<classifier>mac-aarch64</classifier>`

   *after* the version tag, or the UI will not start and the app will crash!
    
7. Create a calculator UI inside `App.java` with the following JavaFX UI classes:
   1. `HsdButton` extends `Button`
      1. call the `super` constructor inside its constructor
      2. set the min width and size to 50 inside its constructor
      3. set the background color to be white inside its constructor
      4. declare this `public` `class` inside a new file `HsdButton.java`
   2. `TextField`
   3. `GridPane`
   4. `BorderPane`
8. Make sure you import the *correct* UI classes from **JavaFX**! Not from AWT or Swing!!!
9. Import and use `ExpressionBuilder` and `Expression` from `net.objecthunter` to calculate the result and display it in the UI
10. Explain verbally how you've built your user interface and why using and understanding maven ist important for Java applications.

### Possible result

*Note: (feel free to adapt and improve the design, add more buttons or use css to improve the styling)*

![](../images/calc.gif)
