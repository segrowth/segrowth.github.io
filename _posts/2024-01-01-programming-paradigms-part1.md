---
title: Programming paradigms - Part 1&#58; Imperative Programming
authors: [imyrta, kjodlows]
date: 2024-01-01 08:00:00 +0100
categories: [Software Engineering, Junior]
tags: [Technical Skills]
image:
  path: /commons/programming-paradigms.png
---

> <b>TODO</b> - Review and rephrase the whole content in accordance with the captions generated for that recording.
{: .prompt-warning }

## Programming Paradigms
Programming Paradigm is a <b>style of programming</b> that guides structure, design and organization of computer 
programs. We have a variety of paradigm types, but the main ones are <b>Imperative</b>, <b>Declarative</b>, and some 
subsets for each of these two e.g. <b>Object-Oriented</b> Programming or quite famous <b>Structuted Query Language</b>
(SQL).

Different programming paradigms may offer <b>alternative approaches</b> that can be more suitable <b>for certain types 
of problems</b>. For example, functional programming is often favored for problems involving data transformations and 
concurrency, while declarative programming can be advantageous for expressing complex business logic.

## Imperative Programming Paradigm

Is a programming style that focus on describing a <b>sequence of steps</b> that a computer must follow to solve a 
problem. It's based on the concept of <b>mutable state</b> and <b>control flow</b>. You define a variable to hold data 
and then use statements and expressions to modify their value. The order of execution is specified by using structures 
such as loops, conditional and function calls. The program usually start with an initial state and while statements are 
executed the state is modified as needed.

> A variety of programming languages support Imperative Programming, from which some examples worth mentioning are: 
Java, Python, C, C++, Javascript, Pascal, Go.
{: .prompt-info }

### Key characteristics

Let's talk about the key characteristics of the Imperative Programming Paradigm. Here we're listing them, along with a
short definition and techniques with which they can be achieved:

> <b>TODO</b> - Check if this content can be organized in another way, e.g. in a table or some unfolding list.
{: .prompt-warning }

State
: Programs maintain mutable state that can be modified during execution.
- Assignments, variable declarations, and updates to variables.

Control Flow
: Programs specify explicit control flow using loops, conditionals, and branching.
- Loops (for, while), conditionals (if-else, switch), and function calls.

Procedures
: Programs are structured as a sequence of procedures or routines that operate on data.
- Subroutines, functions, and procedures to modularize code.

Sequencing
: Programs execute instructions in a particular order.
- By executing statements in the order they appear in the program.

Iteration
: Programs perform repetitive tasks using loops and iteration constructs.
- For loops, while loops, do-while loops, and iterators.

Modularity
: Programs can be divided into smaller, reusable modules.
- Functions, classes, and modules for code organization and reusability.

Control Abstraction
: Programs can encapsulate complex control logic into higher-level abstractions.
- Functions, procedures, and control structures for code abstraction.

Data Structures
: Programs use data structures to organize and manipulate data efficiently.
- Arrays, lists, queues, stacks, trees, and other data structures.

Mutable State
: Programs modify mutable state to reflect changes in the program's execution.
- Variables that can be updated and modified during program execution.

Procedural Abstraction
: Programs can encapsulate functionality into procedures and functions.
- Via procedural decomposition and encapsulation of code into functions and subroutines.

Side Effects
: Imperative programs may have side effects that modify the program's state or external resources.
- Reading from or modifying files, input/output operations, and modifying shared resources.

### Code example

Let's see some of the above concepts in <a href="https://www.jdoodle.com/a/6nWh">a code example</a> in Java:

```java
public class Factorial {
    public static int factorial(int n) {
        int result = 1;
        for (int i = 1; i <= n; i++) {
            result *= i;
        }
        return result;
    }
  
    public static void main(String[] args) {
        int num = 5;
        int fact = factorial(num);
        System.out.println("Factorial of " + num + " is: " + fact);
    }
}
```
> <b>TODO</b> - Describe the example based on <a href="#key-characteristics">the key characteristics list</a>.
{: .prompt-warning }

### Where it's been used?

There's a variety of problems that can be solved by using Imperative Programming, of which we consider the most 
important:

Algorithmic problem solving
: Sorting algorithms, searching algorithms, and mathematical computations can be effectively expressed using imperative
style.

System-level programming
: Imperative programming allows direct manipulation of system components, making it suitable for these tasks like: 
Developing operating systems, device drivers, and low-level software which requires fine-grained control over hardware 
resources and memory management. 

Game development
: Imperative programming provides the control necessary for real-time game logic and rendering pipeline. Building 
interactive games often involves managing complex game states, handling user input, and rendering graphics. 

User interface programming
: Imperative programming allows developers to handle user input events and manage the state of the UI components. 
Graphical user interfaces (GUIs) often involve event-driven programming, where the program responds to user actions and 
updates the interface accordingly.

File and network operations
: Imperative programming is commonly used for tasks involving reading and writing files, sending and receiving network 
requests, and interacting with databases. It allows step-by-step control over I/O operations and managing data 
transformations.

Scripting and automation
: Imperative programming languages are frequently used for scripting and automation tasks. Writing scripts to automate 
repetitive tasks, perform system administration, or process large datasets can be accomplished effectively using an 
imperative approach.

### Summarizing

> <b>TODO</b> - Write a summary.
{: .prompt-warning }

## Conclusion

> <b>TODO</b> - Write a conclusion.
{: .prompt-warning }

## Live discussion

In case you prefer to see a live discussion on the topic see conversation between our colleagues:

> <b>TODO</b> - Replace the embed link when the video is uploaded.
{: .prompt-warning }

{% include embed/youtube.html id='QlQufiDcKSo' %}