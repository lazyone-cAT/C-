# C# Variables — Notes

## Comments

Use `//` for a single-line comment, and `/* */` for a multi-line comment.

```csharp
// this is a single-line comment

/* this is a
   multi-line comment */
```

## What is a Variable?

A variable is a container for storing data values. In C#, some common variable types are:

- `int` — whole numbers
- `double` — floating point numbers
- `char` — a single character
- `string` — a sequence of characters (text)
- `bool` — true/false values

## Creating Variables

To create a variable, specify the type and assign it a value:

```
type variableName = value;
```

- `type` is one of the C# data types (like `int` or `string`)
- `variableName` is the name you give the variable
- the equal sign (`=`) is used to assign a value to the variable

### Example

```csharp
string name = "John";
Console.WriteLine(name);
```

Another example:

```csharp
int myNum = 69;
Console.WriteLine(myNum);
```

### Declaring a Variable Without Assigning a Value

You can declare a variable without assigning a value, and assign it later:

```csharp
int myNum;
myNum = 69;
Console.WriteLine(myNum);
```

### Changing the Value of an Existing Variable

To change the value of an already declared variable, assign a new value using the equal sign:

```csharp
int myNum = 69;
myNum = 6969; // myNum is now 6969
Console.WriteLine(myNum);
```

## Other Types

```csharp
int myNum = 69;
double myDoubleNum = .69D;
char myLetter = 'a';
bool myBool = true;
string myText = "heya";
```

## Constants

If you don't want others to overwrite existing values, use the `const` keyword in front of the variable type.

This declares the variable as constant, which means it becomes **read-only** and unchangeable.

Constants are useful when a variable should always hold the same value, so others can't accidentally break your code.

```csharp
const int myNum = 69;
```

## Displaying Variables

The `Console.WriteLine()` method is often used to display variable values in the console window.

### Combining Text and Variables with `+`

```csharp
string name = "pookie";
Console.WriteLine("I am " + name);
```

You can also use `+` to combine multiple variables:

```csharp
string firstName = "pookie ";
string lastName = "boi";
string fullName = firstName + lastName;
Console.WriteLine(fullName);
```

### Adding Numbers

The `+` character can also be used to add numeric variables together:

```csharp
int x = 69;
int y = 69;
Console.WriteLine(x + y); // outputs 138
```

## Declaring Multiple Variables

You can declare many variables of the same type in one line by separating them with commas:

```csharp
int x = 9, y = 8, z = 69;
Console.WriteLine(x + y + z);
```

### Assigning the Same Value to Multiple Variables

You can also assign the same value to multiple variables in one line:

```csharp
int x, y, z;
x = y = z = 50;
Console.WriteLine(x + y + z);
```

## Identifiers

All C# variables must be identified with a unique name, called an **identifier**.

Identifiers can be short names (like `x` and `y`) or more descriptive names (like `age`, `roll`, `volume`).

```csharp
int myAge = 69;
int a = 69;
```

### Rules for Naming Variables

- Names can contain letters, digits, and the underscore character (`_`)
- Names must begin with a letter or an underscore
- Names should start with a lowercase letter, and cannot contain whitespace
- Names are case-sensitive (`myVar` and `myvar` are different variables)
- Reserved words (C# keywords, such as `int` or `double`) cannot be used as names
