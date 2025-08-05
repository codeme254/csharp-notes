# Switch Statements
Switch statements are a cleaner alternative to else..if.

The switch statement lets you compare a single value against multiple possible matches, and execute different blocks depending on which one it is.

## Basic Syntax
```cs
switch (expression)
{
    case value1:
        // do something
        break;
    
    case value2:
        // do something else
        break;

    default:
        // fallback if no case matches
        break;
}

```

Example:
```cs
class Program
{
    static void Main(string[] args)
    {
        var day = 3;
        switch(day)
        {
            case 1:
                Console.WriteLine("Monda");
                break;
            case 2:
                Console.WriteLine("Tuesday");
                break;
            case 3:
                Console.WriteLine("Wednesday");
                break;
            case 4:
                Console.WriteLine("Thursday");
                break;
            case 5:
                Console.WriteLine("Friday");
                break;
            case 6:
                Console.WriteLine("Saturday");
                break;
            case 7:
                Console.WriteLine("Sunday");
                break;
            default:
                Console.WriteLine("Invalid day");
                break;
        }
    }
}
```
The `default` block executes if no other `case` matches.

## Combining Multiple Cases
You can combine multiple cases if they are doing the same thing:
```cs
class Program
{
    static void Main(string[] args)
    {
        char grade = 'B';

        switch (grade)
        {
            case 'A':
            case 'B':
            case 'C':
                Console.WriteLine("You passed.");
                break;
            case 'D':
            case 'F':
                Console.WriteLine("You failed.");
                break;
            default:
                Console.WriteLine("Invalid grade.");
                break;
        }

    }
}
```