# Gentle Introduction to Programming with Java

### Learning Objectives:

- Understand Java’s core concepts and how it facilitates cross-platform development.
- Explore fundamental Java programming constructs like variables, data types, and basic operators.
- Get hands-on experience with control flow structures (e.g., if-else statements) for decision-making.
- Develop a simple program in Java, reinforcing syntax and logic skills.
- Gain confidence to explore more advanced topics within Java development.

### Introduction

Java is one of the most popular programming languages globally, known for its "Write Once, Run Anywhere" capability,
allowing applications to operate across different platforms without modification. This lesson serves as a
beginner-friendly introduction to programming with Java, covering the essentials of coding, such as variables, data
types, and control flow. As you follow along, you’ll start building a solid foundation in Java that will be crucial as
you progress to more advanced programming concepts.

This lesson is designed for beginner to intermediate Java learners. Basic familiarity with programming concepts will be
helpful but is not required, as we will cover all fundamental aspects in-depth.

Java provides a versatile platform for developing a wide range of applications, from web applications to complex
financial systems. Let’s begin by setting up a simple coding environment using Replit, an online IDE perfect for
practicing Java on any device.

**Accessing Replit:**

- Visit [Replit](https://replit.com/) and create a free account.
- Click create a new Repl.
- Under "Choose a template" select Java and click "Create Repl."

Java code is structured within classes and methods. Here’s a minimal Java program:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}

```

- Class: The `HelloWorld` class is where our code resides.
- Method: main is the starting point of every Java application.
- Output: `System.out.println` prints text to the console.

Explanation: This code outputs "Hello, world!" to the screen, introducing you to Java's syntax and structure.

### Primitive Data Types and Variables

**What is a Variable?**

In Java, a variable is like a container that holds data. Think of it as a labeled box where you can store a piece of
information you’ll need while your program runs. You name this container, which makes it easy to access the information
inside it whenever needed. For example, if you were building a program to calculate grades, you might use variables to
store the scores of different students.

Variables allow us to store and reuse data throughout a program, making it adaptable and useful in many situations. In
Java, each variable is assigned a data type, which defines the kind of information it can hold.

When you create a variable, you declare it by specifying the data type, then giving it a name:

```java
int score;
```

Here, int specifies that score will hold an integer value (a whole number). The variable has been declared, but it
doesn’t yet contain any data until we assign a value to it.

**Assigning Values to Variables**

To store data in a variable, you assign it a value using the `=` operator. After declaration, we can add a value to
score:

```java
score =95;
```

Now, the variable `score` contains the value 95. We can declare and assign values in one line as well:

```java
int score = 95;
```

### Primitive Data Types in Java

Java provides primitive data types for handling basic kinds of data. These types are called "primitive" because they’re
simple, fundamental types that don’t have complex behaviors like objects do. Using these primitive types, you can store
numbers, single characters, and true/false values.

Each primitive type in Java has a specific role, size, and range of values it can hold. Here’s an overview:

- **Integer Types**: These types are used to store whole numbers (no decimals).
    - byte: The smallest integer type, it occupies 1 byte (8 bits) and can store values from -128 to 127.
    - short: Takes up 2 bytes (16 bits), with a range from -32,768 to 32,767.
    - int: The most commonly used integer type, it occupies 4 bytes (32 bits) and stores values from approximately -2
      billion to 2 billion.
    - long: Used for larger numbers, it takes up 8 bytes (64 bits) and can store values up to about 9 quintillion.
- **Floating-Point Types**: These types are used to store numbers with decimal points, essential for precision
  calculations.
    - float: A single-precision floating-point type, occupying 4 bytes. It’s less precise than double but useful when
      memory is limited.
    - double: Double-precision floating-point type, taking up 8 bytes, offering more precision and commonly used for
      scientific and financial calculations.
- **Character Type**: The char type stores a single Unicode character, such as letters, digits, or symbols. It occupies
  2 bytes (16 bits) because it supports a wide range of international characters.
- **Boolean Type**: The boolean type represents true or false values, commonly used in conditions. It takes up very
  little memory.

Java's primitive data types form the backbone of efficient programming, allowing code to run smoothly and consistently
across various systems. Since these types store values directly in memory, they offer speed and simplicity, making your
code more efficient.

Choosing the appropriate data type ensures that your program manages memory wisely and handles data accurately. Here’s
an example of how we can use primitive data types in a real-world program:

```java
public class HelloWorld {
    public static void main(String[] args) {
        int age = 25;          // Integer type
        double salary = 45000.50; // Decimal type
        boolean isEmployed = true; // Boolean type
        System.out.println("Age: " + age);
        System.out.println("Salary: " + salary);
        System.out.println("Employed: " + isEmployed);
    }
}
```

### Decision-Making with `if` and `else`

Control flow structures in Java empower programs to make decisions based on conditions, guiding the program's path.
The `if` and `else` statements are essential tools that allow you to execute different code blocks depending on specific
conditions. This is useful for making logical choices within your program.

Here’s an example program that checks if a number is positive, negative, or zero:

```java
public class NumberCheck {
    public static void main(String[] args) {
        int number = -5;

        if (number > 0) {
            System.out.println("The number is positive.");
        } else if (number < 0) {
            System.out.println("The number is negative.");
        } else {
            System.out.println("The number is zero.");
        }
    }
}

```

In this program:

- The `if` statement checks if the number is greater than zero, indicating it’s positive.
- The `else if` statement checks if the number is less than zero, meaning it’s negative.
- The `else` statement catches all other cases, in this example, when the number is zero.
- This simple decision-making structure makes it easy to handle different outcomes based on the value of number.

### Practical Example: Movie Ticket Pricing System

ACME Movie Theater in New York has hired you to develop a system for calculating movie ticket prices based on age
groups. They aim to offer different pricing tiers to accommodate a diverse audience, with specific discounts for
children, teens, and seniors.

In this program, we need to calculate the cost of a movie ticket depending on the age of the person purchasing it. The
idea
is to offer different pricing tiers based on age groups:

- Child (0-12 years): $5
- Teen (13-17 years): $8
- Adult (18-64 years): $12
- Senior (65+ years): $7

Let’s put this into a Java program where we’ll ask for the user’s age, determine the appropriate pricing category, and
display the ticket price.

```java
import java.util.Scanner;

public class MovieTicketPricing {
    public static void main(String[] args) {
        // Step 1: Create a Scanner object to get input from the user
        Scanner scanner = new Scanner(System.in);

        // Step 2: Prompt the user to enter their age
        System.out.print("Please enter your age: ");
        int age = scanner.nextInt();

        // Step 3: Initialize the ticket price variable
        int ticketPrice;

        // Step 4: First check if age is invalid (negative)
        if (age < 0) {
            System.out.println("Invalid age entered. Please enter a positive age.");
            return;  // Exit the program if the age is invalid
        }
        // Step 5: Determine ticket price based on age using if-else statements
        if (age <= 12) {
            ticketPrice = 5;  // Child price
            System.out.println("Child Ticket: $5");
        } else if (age <= 17) {
            ticketPrice = 8;  // Teen price
            System.out.println("Teen Ticket: $8");
        } else if (age <= 64) {
            ticketPrice = 12;  // Adult price
            System.out.println("Adult Ticket: $12");
        } else {
            ticketPrice = 7;  // Senior price (age >= 65)
            System.out.println("Senior Ticket: $7");
        }

        // Step 6: Display the final price
        System.out.println("Your ticket price is: $" + ticketPrice);

        // Close the scanner to free up resources
        scanner.close();
    }
}

```

**How the Program Works**

1. User Input: The program starts by prompting the user to enter their age. We use `Scanner` to read input from the
   keyboard.
2. Variable Initialization: The `ticketPrice` variable is declared to store the cost of the ticket based on the user’s
   age.
3. Decision-Making with `if-else`: The `if-else` structure checks the age and assigns the correct ticket price:
    - If age is between 0 and 12, the program assigns a ticket price of $5.
    - If age is between 13 and 17, the ticket price is $8.
    - If age is between 18 and 64, the ticket price is $12.
    - If age is 65 or older, the ticket price is $7.
4. Validation: If an invalid age (such as a negative number) is entered, the program displays an error message and
   exits.
5. Display the Result: The final ticket price is displayed to the user, based on the age category.

**Explanation of Key Concepts Used**

- **Variables and Data Types**: We declared an `int` variable, `age`, to hold the user’s age and ticketPrice to hold the
  calculated ticket cost.
- **Control Flow with `if-else`**: The `if-else` statements evaluate the age and assign the appropriate ticket price.
- **User Input with `Scanner`**: `Scanner` was used to get user input directly, making the program interactive.
- **Output Statements**: We used `System.out.println` to guide the user and display the ticket price, making the output
  clear and informative.

This simple movie ticket pricing system is an excellent introduction to Java programming concepts, allowing you to apply
variables, data types, and conditional logic in a meaningful way. By understanding and modifying this program, you can
start creating more complex decision-making systems that build on these foundational skills.

### Summary

In this introductory lesson, you learned the basics of Java, including setting up your environment, using data types,
and controlling program flow with if-else statements. You also built a simple program to practice these concepts.
Understanding these fundamentals will enable you to tackle more advanced Java topics, such as loops, methods, and
object-oriented programming, with confidence.

### Challenges for Further Exploration

- Modify the movie ticket pricing system to include a discount for students (identified by an additional input).
- Create a simple Java program that calculates the sum of all even numbers between 1 and 100.
- Experiment with different data types and control structures, combining them to create mini-programs for various tasks,
  like a basic calculator or a simple guessing game.

### Master Java Programming in 10 Weeks

This comprehensive live, interactive ZOOM course will take you from Java novice to job-ready programmer in just 10
weeks. Here's what you can expect:

**Curriculum Highlights**

- Java fundamentals and syntax
- Object-oriented programming concepts
- Data structures and algorithms
- Exception handling and debugging
- File I/O and database connectivity
- Java Collections Framework
- Multithreading and concurrency
- Java 8+ features (lambdas, streams, etc.)
- Java SE 8 Programmer I (1Z0-808) certification prep

**Career-Focused Outcomes**

- Build a portfolio of real-world Java projects
- Gain confidence for technical interviews
- Develop skills for entry-level Java developer roles
- Prepare for industry-recognized Java certification
- Enhance problem-solving abilities valued by employers

**Why Our Program Works**

- Learn from experienced industry professionals
- Get personalized code reviews and feedback
- Practice with hands-on coding challenges
- Engage in live collaborative coding sessions
- Join a supportive community of peers
- Receive career guidance and job search support

This intensive program is designed to give you the skills, experience and confidence to launch your career as a Java
developer. Through a combination of expert instruction, hands-on practice, and career preparation, you'll be job-ready
in just 10 weeks.
