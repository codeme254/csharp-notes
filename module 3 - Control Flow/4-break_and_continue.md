# `break` and `continue` keywords

## `break`
The `break` keyword terminates the loop:
```cs
class Program
{
    static void Main(string[] args)
    {
        
        for (var i = 1; i <= 10; i++)
        {
            if (i == 5)
            {
                break;
            }
            Console.WriteLine(i);
        }

    }
}
```

## `continue`
The `continue` keyword skips the rest of the loop body for the current iteration and goes to the next iteration.
```cs
class Program
{
    static void Main(string[] args)
    {
        
        for (var i = 1; i <= 10; i++)
        {
            if (i == 5)
            {
                continue;
            }
            Console.WriteLine(i);
            Console.WriteLine(i * 2);
        }                        

    }
}
```