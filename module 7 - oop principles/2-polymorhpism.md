# Polymorphism
Polymorphism refers to the ability to exist in more than one shape.

C# supports two types of polymorphism:
- Compile-time polymorphism (method overloading)
- Runtime polymorphism (method overriding)

## Compile-time polymorphism (method overloading)
Occurs when multiple methods have the same name but different parameters:

```cs
class Calculator
{
    public int Add(int a, int b)
    {
        return a + b;
    }

    public int Add(int a, int b, int c)
    {
        return a + b + c;
    }

    public double Add(double a, double b)
    {
        return a + b;
    }

    public double Add(double a, double b, double c)
    {
        return a + b + c;
    }
}
```

## Run-time polymorphism
This happens when a class provides its own implementation of inherited method.

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
```