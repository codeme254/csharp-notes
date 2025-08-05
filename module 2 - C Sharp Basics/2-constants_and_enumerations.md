# Constants and Enumerations
A constant is a variable whose value never changes.

Use the `const` keyword to decalre constants - `const <type> <name> = <value>;
`
```cs
class Program
{
    static void Main(string[] args)
    {
        const float Pi = 3.142f;
        Console.WriteLine(Pi);
    }
}
```

## Enumerations (Enums) in C#
An enum is a way to define a set of named constants.

Enums are perfect when a variable should only have a fixed set of options.

For example, direction can either be North, South, East or West.

So, instead of:
```cs
string direction = "North";
```

We use enums as follows:

```cs
class Program
{
    enum Direction
    {
        North,
        South,
        West,
        East
    }
    static void Main(string[] args)
    {
        Direction dir = Direction.North;
        Console.WriteLine(dir);
    }
}
```

Behind the scenes, Enums are backed by integers starting from 0:
```cs
enum Direction
{
    North // 0,
    South // 1,
    West // 2,
    East // 3
}
```

You can override the default values:
```cs
class Program
{
    enum Direction
    {
        North = 1000,
        South = 2000,
        West = 3000,
        East = 4000
    }
    static void Main(string[] args)
    {
        int north = (int)Direction.North;
        Console.WriteLine(north);
    }
}
```