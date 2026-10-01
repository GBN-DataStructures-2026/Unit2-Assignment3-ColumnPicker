# Unit 2 - Assignment 3: Column Picker

## Overview
In this final Karel recursive assignment, you will program a robot to analyze a world containing vertical columns of beepers (`RandomColumns.kwld`). Each column starts on Street 2 and extends up to 8 streets high.

Your robot must count the total number of beepers in each column and place a pile containing that exact count at the base of the column on Street 1. The original beeper arrangement in the columns must remain completely unchanged when finished.

---

## World Setup
This project uses a custom world file named `RandomColumns.kwld`. Ensure `RandomColumns.kwld` is placed directly in the root directory of your project folder alongside your `.java` files.

---

## How to Compile and Run

You can run this project using either the VS Code GUI or the integrated terminal.

### Option 1: VS Code GUI (Recommended)
1. Open `Driver.java`.
2. Click the **Play Icon** in the top-right corner, or press `F5`.

### Option 2: Integrated Terminal (Windows)
Because `KarelJRobot.jar` resides in the `lib/` folder, you must explicitly include the classpath (`-cp`) flag when compiling and running from the command line.

Open the integrated terminal in VS Code (`Ctrl + ~`) and run:

```cmd
javac -cp "lib/*;." ColumnPicker.java Driver.java
java -cp "lib/*;." Driver
```

---

## Your Task

Complete `ColumnPicker.java` by implementing recursive methods to count and place beepers across all columns.

### Requirements & Objectives:
1. **Column Processing:** Process each vertical column from Avenue 1 moving East.
2. **State Preservation:** Count all beepers in a column up to 8 streets high, but ensure all original beepers in the column are replaced exactly as they were.
3. **Beeper Placement:** Place a single pile on Street 1 at the base of each column containing the total count of beepers found in that column.
4. **Termination:** Stop processing and turn off when the robot encounters a single indicator beeper placed on Street 1.

---

## Constraints & Rules

* **Strictly No Loops:** You may **not** use `while` or `for` loops anywhere in your implementation. All iteration and counting must be handled recursively.
* **Return-Value Recursion:** Use method return values to pass counts back down the call stack during the unwinding phase.

---

## Troubleshooting & Known Artifacts

* **`FileNotFoundException` for `RandomColumns.kwld`:** Ensure `RandomColumns.kwld` sits in the main assignment folder, not inside `lib/` or `.vscode/`.
* **Closing the GUI Window:** Closing the Karel GUI window after execution finishes may produce a harmless `java.lang.UnsupportedOperationException` in the terminal referencing `Thread.stop()`. This is a legacy artifact of the library on modern Java runtimes and can be safely ignored.