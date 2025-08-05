# Loops
In C#, there are 3 main looping styles:
- `for` - when you know how many times to run.
- `while` - when you want to run as long as a condition is true.
- `do-while` - when you want to run at least once no matter what.

## `for` loop
Used when we know the number of times to loop in advance.

```cs
for (initializer; condition; iterator)
{
    // Code to repeat
}
```

Example:
```cs
class Program
{
    static void Main(string[] args)
    {
        for (var i = 1; i <= 10; i++)
        {
            Console.WriteLine($"Count: {i}");
        }

    }
}
```

## `while` loop
Used when we want to execute the same block of code for as long as a given condition stands:
```cs
class Program
{
    static void Main(string[] args)
    {
        for (var i = 1; i <= 10; i++)
        {
            Console.WriteLine($"Count: {i}");
        }

    }
}
```

```cs
class Program
{
    static void Main(string[] args)
    {
        var i = 1;
        while (i <= 10)
        {
            Console.WriteLine($"Count: {i}");
            i++;
        }

    }
}
```

## `do-while` loop
Used when we want to run the loop at least once regardless the condition:
```cs
do
{
    // Code runs at least once
}
while (condition);
```

```cs
class Program
{
    static void Main(string[] args)
    {
        var i = 10;

        do
        {
            Console.WriteLine($"Count: {i}");
            i++;
        }
        while (i <= 5);


    }
}
```