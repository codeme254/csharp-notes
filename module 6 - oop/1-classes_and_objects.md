# Classes and Objects

A class is a blueprint for an object.

It defines what an object knows (fields/properties) and what it can do (methods).

There are three core organs of a class:
- Fields
- Properties
- Methods

## Declaring a Class

```cs
class Person
{
    public string FirstName;
    public string LastName;

    public void greet()
    {
        Console.WriteLine($"Hello, my name is {FirstName} {LastName}");
    }
}
```

An object is an actual instance of a class.
```cs
class Person
{
    public string FirstName;
    public string LastName;

    public void greet()
    {
        Console.WriteLine($"Hello, my name is {FirstName} {LastName}");
    }
}

class Program
{
    static void Main(string[] args)
    {
        Person p1 = new Person();
        p1.FirstName = "John";
        p1.LastName = "Doe";
        p1.greet();
    }
}
```