# Type Conversion
Type conversion refers to changing a value from one data type to another.

There are two flavors of type conversion in C#:
- Implicit Conversion
- Explicit (type casting)

## Implicit Conversion
Here, C# handles the type conversion for you.

It is done automatically when passing a smaller size type to a larger size type (it's like pouring a cup of water into an empty bucket).

```cs
class Program
{
    static void Main(string[] args)
    {
        int myint = 35;
        double myDouble = myint;
        Console.WriteLine(myint);
        Console.WriteLine(myDouble);
    }
}
```

## Explicit Conversion (Type Casting)
Explicit conversion (casting) is done manually by placing the type in parenthesis in front of the value.

With explicit conversion, there's a chance of data loss.

```cs
class Program
{
    static void Main(string[] args)
    {
        double myDouble = 3.99;
        int myInt = (int)myDouble;

        Console.WriteLine(myInt);
        Console.WriteLine(myDouble);
    }
}
```

## Conversion Using the `Convert` Class
If you want conversions that include error checking and work with strings and other types, use the `Convert` class.

```cs
class Program
{
    static void Main(string[] args)
    {
        int myInt = 10;
        double myDouble = 5.25d;
        bool myBool = false;

        Console.WriteLine(Convert.ToString(myInt));
        Console.WriteLine(Convert.ToDouble(myInt));
        Console.WriteLine(Convert.ToInt32(myDouble));
        Console.WriteLine(Convert.ToString(myBool));
    }
}
```