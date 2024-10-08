## Course 4: JavaFX
______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the `H:\` drive!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______

### Topic

Java FX Graphical user interface (GUI) visualizing a lottery drawing.

### Tasks

1. Create the Maven project ```git4c4``` by using the archetype `javafx-archetype-simple` from `org.openjfx` to create a **JAVA FX** (not Swing!) application
2. Extend the Code in `App.java` and create a GUI consisting of 6 [TextFields](https://openjfx.io/javadoc/17/javafx.controls/javafx/scene/control/TextField.html)'s and one "Draw" [Button](https://openjfx.io/javadoc/17/javafx.controls/javafx/scene/control/Button.htmll). Fill the `TextFields` with random numbers between 1 and 49 via the ```Random``` class from ```util.Random```. Use your matriculation number as seed for the Random Number Generator.
3. Implement the following features:
    - No number is drawn more than once
    - All numbers are in ascending order
4. Explain why Maven is used in this context and how it makes software development easier.

![lotto](../images/21_lotto.png)
