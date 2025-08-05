# Method Parameters and Return Values

## Parameters and Arguments
Information can be passed to methods as parameter. Parameters act as variables inside the method.

They are specified after the method name, inside the parentheses. You can add as many parameters as you want, just separate them with a comma.

When a parameter is passed to the method, it is called an **argument**.

```cs
class Program
{
    public static void Greet(string firstName, string lastName)
    {
        Console.WriteLine($"Hello {firstName} {lastName}");
    }
    static void Main(string[] args)
    {
        Greet("John", "Doe");
        Greet("Jane", "Doe");
    }
}
```

### Default Parameters
You can also use default parameters by using the equal sign.

If you call the method without an argument, it will use the default value you specified.
```cs
class Program
{
    public static void Greet(string name = "Guest")
    {
        Console.WriteLine($"Hello {name}");
    }
    static void Main(string[] args)
    {
        Greet(); // Hello Guest
        Greet("John"); // Hello John
    }
}
```

### Named Arguments
It is also possible to send arguments with the `key:value` syntax:

```cs
class Program
{
    static void Add(int a, int b, int c)
    {
        Console.WriteLine(a + b + c);
    }
    static void Main(string[] args)
    {
        Add(b: 33, c:99, a: 400);
    }
}
```

## Return values
If you want the method to return a value, you can use a primitive data type (such as `int` or `double`) instead of void, 
and use the `return` keyword inside the method:
```cs
class Program
{
    public static int add(int a, int b)
    {
        return a + b;
    }

    public static float divide(int a, int b)
    {
        return a / b;
    }
    static void Main(string[] args)
    {
        Console.WriteLine(add(5, 6));
        Console.WriteLine(divide(8, 3));
    }
}
```