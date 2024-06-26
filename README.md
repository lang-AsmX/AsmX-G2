# AsmX G2

# Installation
To install AsmX G2, run the following command:
```bash
cd src && npm install
cd ../
```

# Usage
To run AsmX G2, run the following command:
```bash
# Windows
asmx /examples/hello.asmx

# Linux
asmx //examples/hello.asmx
```

## Table of Contents
- [Chapter 1: Introduction to AsmX G2](#chapter-1-introduction-to-asmx-g2)
- [Chapter 2: Setting Up the Development Environment](#chapter-2-setting-up-the-development-environment)
- [Chapter 3: Basic Syntax and Structure](#chapter-3-basic-syntax-and-structure)
- [Chapter 4: Updating AsmX G2](#chapter-4-updating-asmx-g2)


## Chapter 1: Introduction to AsmX G2
AsmX G2 is a powerful, low-level programming language designed for efficient and precise control over system resources. It combines the speed and flexibility of assembly language with modern programming constructs, making it an ideal choice for system-level programming, embedded systems, and performance-critical applications.

In this comprehensive guide, we will explore the intricacies of AsmX G2, starting from the basics and gradually progressing to advanced topics. Whether you are a beginner or an experienced programmer, this book will provide you with the knowledge and skills necessary to master AsmX G2 programming.

## Chapter 2: Setting Up the Development Environment
Before diving into the world of AsmX G2 programming, it is essential to set up a proper development environment. In this chapter, we will guide you through the process of installing and configuring the necessary tools and dependencies.

### Prerequisites
To begin programming in AsmX G2, you will need the following:
- NodeJS (v18.16.1 or higher)
- Git Bash
- A text editor or Integrated Development Environment (IDE) such as VSCode

### Installation Steps
1. Download and install NodeJS from the official website (https://nodejs.org). Make sure to select the appropriate version for your operating system.
2. Download and install Git Bash from the official website (https://git-scm.com).
3. Download and install VSCode or your preferred text editor/IDE.

### Cloning the AsmX G2 Repository
To access the AsmX G2 source code and examples, you need to clone the official repository from GitHub. Open Git Bash and execute the following command:
```
git clone https://github.com/lang-AsmX/AsmX-G2.git
```

Once the repository is successfully cloned, navigate to the `src` directory and install the necessary dependencies by running the following commands:
```
cd src && npm install
cd ../
```

Congratulations! You have now set up your AsmX G2 development environment and are ready to start programming.

## Chapter 3: Basic Syntax and Structure
In this chapter, we will explore the fundamental syntax and structure of AsmX G2 programs. Understanding these concepts is crucial for writing well-organized and efficient code.

### The Main Function
Every AsmX G2 program must have a `main` function, which serves as the entry point of the program. The `main` function is defined using the `@function` keyword followed by the function name and a pair of parentheses. Here's an example:
```
@function main() {
  ;; Your code goes here
}
```

It is important to note that AsmX G2 executes the `main` function only when it encounters its definition. Re-declaring the `main` function will result in an error.

### Comments
Comments in AsmX G2 are denoted by the `;;` symbol. Any text following the `;;` symbol on a line is considered a comment and is ignored by the compiler. Comments are useful for adding explanatory notes and improving code readability. For example:
```
;; This is a single-line comment
```

### Hello, World! Program
Let's write our first AsmX G2 program, the classic "Hello, World!" example. Open your text editor or IDE and create a new file with the following code:
```
@function main() {
  @push "Hello, World!";
  @system 4;
}
```

Let's break down the code:
- The `@push` instruction takes a single argument, which in this case is a string literal. It pushes a pointer to the string onto the stack.
- The `@system` instruction takes a single argument of type `number`. It allows you to make system calls. In this example, the argument `4` indicates that we want to perform a standard output (stdout) operation.

Before printing, the `@system` instruction retrieves the last element from the stack, which is a 16-bit pointer, and uses it to read from memory. The stack exclusively stores 16-bit pointers.

To run the program, save the file and execute the following command in Git Bash:
```
asmx your_file_name.asmx
```

Congratulations! You have just written and executed your first AsmX G2 program.

## Chapter 4: Updating AsmX G2

AsmX G2 now includes a convenient command to update to the latest version. To use this feature, simply run:
```
asmx update
```
This command will:

1. Check for the latest stable version of AsmX G2
2. Download the new version if available
3. Install the update
4. Restart the AsmX G2 service (if applicable)

### Notes:
- Ensure you have an active internet connection when running the update command.
- The update process may require administrative privileges, depending on your system configuration.
- It's recommended to back up your current AsmX G2 configuration before updating.
- If you encounter any issues during the update process, please refer to our troubleshooting guide or open an issue on our GitHub repository.
