# Method Overloading
With method overloading, multiple methods can have the same name with different parameters:

```cs
class Program
{
    static int Add(int a, int b)
    {
        return a + b;
    }
    static int Add(int a, int b, int C)
    {
        return a + b + C;
    }

    static int Add(int a, int b, int c, int d)
    {
        return a + b + c + d;
    }
    static void Main(string[] args)
    {
        Console.WriteLine(Add(1, 2));
        Console.WriteLine(Add(1, 2, 3));
        Console.WriteLine(Add(1, 2, 3, 4));
    }
}
```