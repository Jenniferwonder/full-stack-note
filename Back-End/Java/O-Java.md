---
Title: O-Java
Type: O
tags:
  - Java
DateStarted: 2023-10-27
DateModified: 2023-10-29
status: 
mindmap-plugin: basic
---

# Java

## Reference

### [Hello World](https://introcs.cs.princeton.edu/java/11hello/)

## IntelliJ IDEA

### Config
- Auto-format: [Code Formatting in IntelliJ IDEA - YouTube](https://www.youtube.com/watch?v=vjVWjocENLg&t=118s)
- Low disk space:
    - [解决 IntelliJ IDEA占用C盘过大空间问题\_idea 项目索引空间占用-CSDN博客](https://blog.csdn.net/weixin_44449518/article/details/103334235?spm=1001.2101.3001.6661.1&utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-103334235-blog-111880716.235%5Ev38%5Epc_relevant_anti_t3_base&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-103334235-blog-111880716.235%5Ev38%5Epc_relevant_anti_t3_base&utm_relevant_index=1)
    - [IntelliJ IDEA的解决占用C盘问题\_idea low disk space-CSDN博客](https://blog.csdn.net/qq_37279783/article/details/111880716)

### Plugin Installation
- [GitHub - pmd/pmd: An extensible multilanguage static code analyzer.](https://github.com/pmd/pmd)
- [Running SpotBugs — spotbugs 4.8.0 documentation](https://spotbugs.readthedocs.io/en/latest/running.html)
- WakaTime API: waka_f89ebcfc-d562-421a-8993-50c3e9a4904b

### Shortcuts
- Auto Format: `CTRL ALT L`
- Set code block format/ Bug quick fix: `ALT ENTER`
- Delete a line: `CTRL L`
- Move lines up: select and `CTRL SHIFT UP`

## Basics
### Set up environment
- Download JDK: [Home | Adoptium](https://adoptium.net/) 
### Compile and Run
- 解压：`jar xf stdlib.jar`
- classpath
    - `javac -cp .:/stdlib.jar Barnsley.java`
    - `java -cp .:/stdlib.jar Barnsley 10000`

### Lib
- Java Math Lib
    - [Math (Java Platform SE 8 )](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html)

## Data Types

### Read integers from a command line:
- `Integer.parseInt(args[0])`

### Read floating point numbers from a command line:
- `Double.parseDouble(args[0])`

### Define and print out a Boolean value
- ![[O-Java-Boolean.png|325]]

### Static cast: cast a data type to a value

## Operators

### Assignment Operator

### Comparison Operator

### Boolean Operator

## Control Flow

### Conditionals

### Loops

## Arrays

### ![[O-Java-Array.png|475]]

## Input and Output

### Print from a new line:
- `println` or `\n`