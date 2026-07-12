# C# Output / Printing - A Beginner's Guide

In C#, displaying text, numbers, to the user is done through the `Console` class. This guide covers the two primary methods: `WriteLine()` and `Write()`.

---

## The `WriteLine()` Method

The `WriteLine()` method is used to **print text or data to the console**. The key feature of this method is that it **automatically inserts a new line (`\n`) at the end** of the output. This means every subsequent output will appear on a fresh line.

### Basic Text Output
You can print any text by placing it inside double quotes `""`.

```csharp
Console.WriteLine("Hello World!");
Console.WriteLine("I am Learning C#");
Console.WriteLine("It is awesome!");
```

**Output:**
```
Hello World!
I am Learning C#
It is awesome!
```

### Outputting Numbers
You can pass numbers directly to `WriteLine()` without quotes.

```csharp
Console.WriteLine(100);
Console.WriteLine(3.14);
```

**Output:**
```
100
3.14
```

### Performing Mathematical Calculations
The `WriteLine()` method can evaluate expressions before printing the result.

```csharp
Console.WriteLine(1 + 2);      // Outputs: 3
Console.WriteLine(10 * 5);     // Outputs: 50
Console.WriteLine(20 - 8);     // Outputs: 12
Console.WriteLine(15 / 3);     // Outputs: 5
```

**Output:**
```
3
50
12
5
```

> **Note:** C# respects standard mathematical operator precedence (multiplication/division before addition/subtraction). You can use parentheses `()` to group operations: `Console.WriteLine((2 + 3) * 4);` → Outputs `20`.

---

## The `Write()` Method

The `Write()` method works almost exactly like `WriteLine()`, with **one important difference**—it does **not** add a new line at the end. This means subsequent output will continue on the **same line**.

```csharp
Console.Write("Hello World! ");
Console.Write("It will print on the same line.");
Console.Write(" Here is another piece.");
```

**Output:**
```
Hello World! It will print on the same line. Here is another piece.
```

### Mixing Both Methods
You can combine `Write()` and `WriteLine()` to control exactly how your text is formatted.

```csharp
Console.Write("First part, ");
Console.Write("second part, ");
Console.WriteLine("third part with a new line.");
Console.Write("This starts on a new line because of the previous WriteLine!");
```

**Output:**
```
First part, second part, third part with a new line.
This starts on a new line because of the previous WriteLine!
```

---

## Combining Text and Numbers

You can also output a mix of static text and calculated results directly.

```csharp
Console.WriteLine("The sum of 5 and 3 is: " + (5 + 3));
```

**Output:**
```
The sum of 5 and 3 is: 8
```

*(The `+` operator concatenates strings and numbers together in this context.)*

---

## Quick Reference Table

| Method | Description | Adds a New Line? |
| :--- | :--- | :---: |
| `Console.WriteLine("text");` | Prints text and moves cursor to the next line. | ✅ Yes |
| `Console.Write("text");` | Prints text and leaves cursor on the same line. | ❌ No |
| `Console.WriteLine(123);` | Prints a number and moves to the next line. | ✅ Yes |
| `Console.WriteLine(5 + 5);` | Prints the result of a calculation and moves to the next line. | ✅ Yes |

---

## Key Takeaways

- Use **`WriteLine()`** when you want each output on its own line.
- Use **`Write()`** when you want to build a continuous line of output.
- You can print **both text and numbers** directly without any special conversion.
- C# can **perform math calculations** right inside the `WriteLine()` or `Write()` parentheses.
- The output is sent to the **console/terminal**, which is the default window where your program runs.

---

## Try It Yourself

Copy the following code into a `.cs` file and run it to see all these concepts in action:

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        // Using WriteLine
        Console.WriteLine("=== Using WriteLine ===");
        Console.WriteLine("Hello");
        Console.WriteLine("World");
        Console.WriteLine(10 + 20);
        
        // Using Write
        Console.WriteLine("\n=== Using Write ===");
        Console.Write("Hello ");
        Console.Write("World ");
        Console.Write("on one line!");
        
        // Mixed usage
        Console.WriteLine("\n\n=== Mixed Example ===");
        Console.Write("Result of 2 * 8 = ");
        Console.WriteLine(2 * 8);
    }
}
```

**Expected Output:**
```
=== Using WriteLine ===
Hello
World
30

=== Using Write ===
Hello World on one line!

=== Mixed Example ===
Result of 2 * 8 = 16
```

