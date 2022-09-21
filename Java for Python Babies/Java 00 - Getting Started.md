# Java 0 - Getting Started

## What is Java

Java is an **Object-Oriented Programming** (OOP) language. That basically means that you are forced into the OOP paradigm. Procedural or functional programming - the style of programming you'll most probably be used to - are possible, but aren't recommended.

We'll discuss OOP concepts later on, so for now let's just get your environment set up.

## Environment

Ensure you have the following installed - see the footnotes for more information.

| Name     | Link                                                                                      | Footnote |
| -------- | ----------------------------------------------------------------------------------------- | -------- |
| JDK      | [Oracle](https://www.oracle.com/uk/java/technologies/javase/jdk11-archive-downloads.html) | [1]      |
| Netbeans | [Netbeans](https://netbeans.apache.org/)                                                  | [2]      |

[1]

Java requires the Java Development Kit (JDK) in order to compile and run any code you write. There are multiple versions, but (as far as I'm aware) version 11 is used for the course. **JDK is not backwards compatible** so you will need to install the right version(s). You **can have multiple JDK versions though**.

[2]

Netbeans is a really ugly, stone-aged IDE that you'll unfortunately be using during the course (unless they've changed that). While other options are available, like IntelliJ, there are issues with project compatibility between the two.

Markers use Netbeans, so I recommend sticking to it if you want things to go smoothly.  

## Navigating Netbeans, The Rebranded Hell

### Create a New Project

Java, being an OOP language, has a **lot** of boilerplate code. But don't worry, Netbeans can write most of it for you. The first thing you need to know is how to create a **project**. 

1. go to `File > New Project` to begin creating a project. 

2. Select `Java with Maven` then `Java Application` and click next.

3. Give your project a name, and change the `Project Location` if you'd like

4. Click Finish

Your project will now be created.

### Where to Find Your Source Code

On the left-hand side, you should see an explorer view of your `Projects`. The little red cup![](C:\Users\Adam\AppData\Roaming\marktext\images\2022-07-30-18-50-46-image.png) is your **project**, and any child folders or files are part of that project. As I said, a lot of it is boilerplate and you should leave it alone.

Right click the ![](C:\Users\Adam\AppData\Roaming\marktext\images\2022-07-30-18-50-30-image.png) and select `New > New Java Main` this will generate the entry point of the program, the **main class**.

#### Main Class

The **main class** is the entry-point of your program. When you hit run ![](C:\Users\Adam\AppData\Roaming\marktext\images\2022-07-31-03-56-20-image.png), the code will begin executing **from the main method**.

```java
public class Main {
    public static void main(String[] args) {
        // TODO code application logic here
    }
}
```

You can ignore most of this for now, all you need to know is that you should put your code **where the `// TODO code application logic here` is**.

For the sake of teaching the most basic syntax, we'll only be coding in the main method.

### Printing to the Console

In Python, a simple `print("Hello World!")` would suffice. Java, being Java, is not as concise

```java
System.out.println( "Hello World!" );
```

Note the use of `;`. You'll need to end practically every line with one, otherwise you'll get an error.

Don't worry, Netbeans has a snippet (a shortcut) for this. type `sout` and hit tab to generate this line of code.

### Getting User Input

Again, Python has it easy. `input( "message to display to the console: " )`. Java, not so much.

```java
Scanner sc = new Scanner( System.in );

System.out.println( "message to display to the console: " )
String input = sc.nextLine();
```

`Scanner` is **not in Java by default**, you will need to import it. Netbeans will notify you with this icon when you are missing an import. Click the icon, then `Add import for java.util.Scanner` to automatically import `Scanner`.
