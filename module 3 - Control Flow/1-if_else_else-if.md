# if, else, else if

## `if` statement

```cs
class Program
{
    static void Main(string[] args)
    {
        var age = 35;
        if (age > 18)
        {
            Console.WriteLine("You are an adult");
        }
    }
}
```

## `else`
```cs
class Program
{
    static void Main(string[] args)
    {
        var age = 15;
        if (age > 18)
        {
            Console.WriteLine("You are an adult");
        } else
        {
            Console.WriteLine("You are under age");
        }
    }
}
```

## `else if`
```cs
class Program
{
    static void Main(string[] args)
    {
        var score = 55;
        if (score >= 90)
        {
            Console.WriteLine("A");
        } else if (score >= 50 && score < 90)
        {
            Console.WriteLine("B");
        } else if (score >= 30 && score < 50)
        {
            Console.WriteLine("C");
        } else
        {
            Console.WriteLine("D");
        }
    }
}
```