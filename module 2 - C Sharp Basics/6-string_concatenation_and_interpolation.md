# String Concatenation and Interpolation

In many applications, it becomes necessary to construct dynamic text by combining fixed strings with variable data.

C# provides two primary mechanisms to accomplish this:
- String concatenation
- String interpolation

## String Concatenation
String concatenation involves joining multiple strings together using the `+` operator:
```cs
class Program
{
    static void Main(string[] args)
    {
        var fullName = "John Doe";
        Console.WriteLine("My full name is "+fullName);
    }
}
```

While straightforward, it can become cumbersome and less readable when dealing with complex or lengthy output.
```cs
class Program
{
    static void Main(string[] args)
    {
        var firstName = "John";
        var lastName = "Doe";
        var age = 35;
        var occupation = "plumber";
        Console.WriteLine("My name is " +firstName +lastName+ " I am " +age+ " years old and I am a " +occupation);
    }
}
```

## String Interpolation
String interpolation, introduced in C# 6.0, offers a more concise and readable syntax for embedding expressions directly within string literals.

Just prefix your string with `$` and put variable names inside `{}`.
```cs
class Program
{
    static void Main(string[] args)
    {
        var firstName = "John";
        var lastName = "Doe";
        var age = 35;
        var occupation = "plumber";
        Console.WriteLine($"My name is {firstName} {lastName}, I am {age} years old and I am a {occupation}.");
    }
}
```