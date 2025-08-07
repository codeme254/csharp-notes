# Inheritance
Inheritance let's you create a new class based on an existing class.

The new class is called the **derived class** and it inherits members (fields, properties and methods) from the existing class which is called the **base class**.

Here is the basic syntax:
```cs
// Base class
class Animal
{
    public void Eat()
    {
        Console.WriteLine("Animal eating");
    }
}

// Derived class
class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Dog barking");
    }
}

class Program
{
    static void Main(string[] args)
    {
        Dog d = new Dog();
        d.Bark();
        d.Eat();
    }
}
```

## Overriding methods
You can override methods in the derived class.

To do this, use `virtual` keyword in the base class on the method and the use `override` keyword in the derived class method.

```cs
class Animal
{
    public virtual void Eat()
    {
        Console.WriteLine("Animal eating");
    }
}

class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Dog barking");
    }

    public override void Eat()
    {
        Console.WriteLine("Dog is eating");
    }
}
class Program
{
    static void Main(string[] args)
    {
        Dog d = new Dog();
        d.Bark();
        d.Eat(); // Dog is eating
    }
}
```

## Sealed classes and methods
To prevent a class from being inherited or a method from being overridden, use the `sealed` keyword.

```cs
sealed class Animal
{
    public void Eat()
    {
        Console.WriteLine("Animal eating");
    }
}
```