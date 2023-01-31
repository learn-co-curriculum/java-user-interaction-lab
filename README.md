# User Interaction Lab

## Learning Goals

- Practice using the `Scanner` to take in user input.
- Process and display user input.
- Practice using `try-catch` blocks to catch `InputMismatchExceptions`.

## Introduction

In this lab, practice using the `Scanner` to take in different user input from
the console. You also will have the option of using a `try-catch` block to catch
`InputMismatchException` errors that could be thrown.

Fork and clone this repository. When you do, you will see a `Lab.java` file.
Like the "Operators Lab" you worked on previously, this is where you will put
all of your code. Note the comments in the file as well. This should provide a
basic layout of where to put certain parts of your code.

## Instructions

Assume you run a market. You want to ask the user to add a fruit to the market
and then add a quantity and price. For example: 5 apples cost $4.25.

Write a program to take in the fruit, the quantity of that fruit, and how much
that quantity of fruit may cost. Here is a sample output:

![sample-output](https://curriculum-content.s3.amazonaws.com/java-mod-1/user-interaction-lab/user-interaction-sample-output.png)

Follow the instructions below when writing the program:

- Create a `Scanner` as seen in the "User Interaction" lesson.
- Use `System.out.println()` to prompt the user for a type of fruit.
  - The message that prints out to the user should be: "Please enter a String to
    represent the fruit you want to add to the market:".
- Store the user's input in a `String` variable called `fruit`.
  - HINT: The program should be able to take in a fruit named "passion fruits".
    Consider the differences between the methods `next()` and `nextLine()`.
    - `next()` scans the next token until it sees a space.
    - `nextLine()` scans the next token until it sees a newline.
- Use `System.out.println()` to prompt the user for a quantity.
  - The message that prints out to the user should be: "Please enter the
    quantity of " + fruit + ":".
  - Note the combination of `Strings` used in this `println()`!
- Store the user's input in a `int` variable called `quantity`.
- Use `System.out.println()` to prompt the user on the cost of the fruit.
  - The message that prints out to the user should be: "Please enter the price
    of how much " + quantity + " " + fruit + " will cost:".
  - Note the combination of `Strings` used again!
- Store the user's input in a `double` variable called `price`.
- Uncomment the line:
  `System.out.println(quantity + " " + fruit + " cost $" + price);`

Run the program after you finished completing the above instructions. Remember,
you can run the program as much as you want to ensure the output is what you
expect.

You may also run the program with the debugger to see the variables in the Java
Visualizer.

### Optional Task

> You cannot perform this task until the original lab assignment is completed.

Optionally, add a `try-catch` block to the lab assignment. The `try-catch` block
can be implemented in a similar fashion to the "Exception Handling" lesson.

It should catch an `InputMismatchException` exception. If the exception is
caught, print out a message using `System.out.println()` that states: "The input
entered was not in the correct format".

If any of the user input entered threw an `InputMismatchException`, then the
output could look like this:

![try-catch-sample-output](https://curriculum-content.s3.amazonaws.com/java-mod-1/user-interaction-lab/user-interaction-lab-try-catch-output.png)

## Expected Output

Here are some tests you can run and the expected output:

```text
Assume you run a market. We want to add a fruit, a quantity, and how much that fruit will cost.
For example: 5 apples cost $4.25.

Please enter a String to represent the fruit you want to add to the market:
apples
Please enter the quantity of apples:
5
Please enter the price of how much 5 apples will cost:
4.25
5 apples cost $4.25
```

```text
Assume you run a market. We want to add a fruit, a quantity, and how much that fruit will cost.
For example: 5 apples cost $4.25.

Please enter a String to represent the fruit you want to add to the market:
lemons
Please enter the quantity of lemons:
4
Please enter the price of how much 4 lemons will cost:
2.50
4 lemons cost $2.5
```

```text
Assume you run a market. We want to add a fruit, a quantity, and how much that fruit will cost.
For example: 5 apples cost $4.25.

Please enter a String to represent the fruit you want to add to the market:
passion fruits
Please enter the quantity of passion fruits:
1
Please enter the price of how much 1 passion fruits will cost:
0.65
1 passion fruits cost $0.65
```
