# C# Hello World - A Beginner's Guide

This repository contains a classic "Hello World" program written in C#. It serves as the perfect starting point for understanding the fundamental building blocks of the C# programming language.

## The Code

The entire program is contained within a single file, conventionally named `hello.cs`. 

```csharp
using System;

namespace HelloWorld
{
    class Hello
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World");
        }
    }
}
```

---

## Step-by-Step Breakdown

### 1. The `using` Directive (Importing Libraries)
```csharp
using System;
```
- **What it does:** This tells the compiler, *"Hey, I want to use code from the `System` namespace."*
- **Why we need it:** The `Console` class (which we use to print text) lives inside the `System` namespace. Without this line, we would have to type `System.Console.WriteLine()` every time. This directive lets us write the shorter version (`Console.WriteLine`).

### 2. The `namespace` Declaration (Organizing Code)
```csharp
namespace HelloWorld
```
- **What it does:** Namespaces are like **containers** used to organize your code.
- **Why we need it:** When working on large projects with hundreds of classes, namespaces prevent **naming collisions**. For example, you could have `MyProject.Data.User` and `MyProject.Models.User`—both named `User`, but living in different namespaces so the compiler knows exactly which one you mean.

### 3. The Curly Braces `{ }` (Defining Boundaries)
- **What they do:** Curly braces mark the **beginning** and **end** of code blocks.
- **Why we need them:** They tell the compiler exactly where your namespace, class, or method starts and stops. The compiler completely ignores blank lines, extra spaces, and indentation—you could technically write the whole program on one messy line, but using braces keeps it readable for humans!

### 4. The `class` Container (The Heart of C#)
```csharp
class Hello
```
- **What it does:** A **class** is a container that holds both **data** (variables) and **actions** (methods).
- **Why we need it:** C# is a **strictly object-oriented language**. This means that **every single line of executable code must live inside a class**. You cannot write "floating" code outside of a class like you can in Python or JavaScript. 
- **Note on naming:** While you can name it anything (e.g., `Program` in standard templates), we named it `Hello` here. It is a best practice to name classes using **PascalCase** (capitalizing the first letter).

### 5. The `Main` Method (The Entry Point)
```csharp
static void Main(string[] args)
```
- This is the **entry point** of your application. When you run the program, the computer looks for this exact method signature and starts executing the code inside it.
  - `static` means we don't need to create an instance of the class to run it.
  - `void` means it doesn't return any data.
  - `string[] args` allows you to pass command-line arguments into the program.

### 6. The Output Command
```csharp
Console.WriteLine("Hello World");
```
- This line actually prints the text to the console/terminal. 
- `WriteLine` prints the text and moves the cursor to the next line (unlike `Write`, which stays on the same line).

---

## How to Run This Program

### Option 1: Using .NET SDK (Recommended)
1. Open your terminal or command prompt.
2. Navigate to the folder containing `hello.cs`.
3. Run the following commands:
   ```bash
   dotnet new console   # Only needed if you don't have a .csproj file
   dotnet run
   ```

### Option 2: Using the Classic C# Compiler (csc)
If you have the .NET Framework SDK installed:
```bash
csc hello.cs
hello.exe
```

---

## Key Takeaways

- `using` = Borrowing tools from a library.
- `namespace` = Organizing code and preventing naming conflicts.
- `class` = The mandatory container for all C# code.
- `Main()` = The starting point of every C# program.
- C# ignores whitespace, but **curly braces `{}`** are essential to define structure.
