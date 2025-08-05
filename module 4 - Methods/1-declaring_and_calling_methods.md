A method is a block of code that only runs when it is called.

You can pass data known as **parameters**, into a method.

Method are used to perform certain actions, methods are also called **functions**.

We use methods to reuse code, define the code once and run it as many times as we want to.

## Creating a method
A method is defined by the name of the method followed by parenthesis.

```cs
class Program
{
    static void SayHello()
    {
        Console.WriteLine("Hello, World");
    }
}
```
- `SayHello`: name of the method
- `static`: means the the method belongs the to `Program` class and not an object of the Program class.
- `void`: means the the method does not return anythin.

The convention in C# is to start your method names with uppercase letter.

You can also specify the access modifier - `public`, `private`, `protected` (more about this later).
```cs
class Program
{
    public static void SayHello()
    {
        Console.WriteLine("Hello, World");
    }
}
```

## Calling a method
To call (execute) a method, write the method's name followed by two parentheses () and a semicolon.

```cs
class Program
{
    public static void SayHello()
    {
        Console.WriteLine("Hello, World");
    }
    static void Main(string[] args)
    {
        SayHello();
        SayHello();
    }
}
```