# Constructors
A constructor is a special method that runs automatically when you create a new object.

It is used to:
- initialize new values (fields or properties).
- set up dependencies.
- do anything the object needs to do before being used.

## Basic syntax for a constructor

```cs
class Person
{
    public string FirstName;
    public string LastName;

    // Constructor
    public Person()
    {
        FirstName = "Unknown";
        LastName = "Unknown";
    }

    public void greet()
    {
        Console.WriteLine($"Hello, my name is {FirstName} {LastName}");
    }
}
```
Here, when we create an object from the class, it starts with the FirstName and LastName set to "unknown".

## Parameterized Constructor
We can pass parameters to our constructors:
```cs
class Person
{
    public string FirstName;
    public string LastName;

    public Person(string userFirstName, string userLastName)
    {
        FirstName = userFirstName;
        LastName = userLastName;
    }

    public void greet()
    {
        Console.WriteLine($"Hello, my name is {FirstName} {LastName}");
    }
}
```

We can the use the class as follows:
```cs
Person p1 = new Person("John", "Doe");
```

## Constructor Overloading
You can define more than one constructor with different parameters.

This is called **constructor overloading**.

```cs
class Person
{
    public string FirstName;
    public string LastName;

    // First constructor
    public Person()
    {
        Console.WriteLine("Creating a user");
    }

    // Second constructor
    public Person(string firstName)
    {
        Console.WriteLine($"{FirstName} is an awesome person");
    }

    // Third constructor
    public Person(string userFirstName, string userLastName)
    {
        FirstName = userFirstName;
        LastName = userLastName;
    }

    public void greet()
    {
        Console.WriteLine($"Hello, my name is {FirstName} {LastName}");
    }
}
```

## Default constructor
If you don't define any constructor, C# automatically gives you a default one like:

```cs
public Person() { }
```

But if you define any constructor yourself, the default won't be auto-generated.