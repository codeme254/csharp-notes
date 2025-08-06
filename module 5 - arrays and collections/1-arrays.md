# Arrays

Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

In C#, an array is a fixed size, ordered collection of elements of the same type.

## Declaring an array
Declare an array as shown:
`type[] arrayName = new type[size]`

```cs
class Program
{
    static void Main(string[] args)
    {
        int[] numbers = new int[5]; // array with 5 elements
        Console.WriteLine(numbers);
    }
}
```

### Initializing an array with values
```cs
class Program
{
    static void Main(string[] args)
    {
        int[] scores = new int[5] {10, 20 ,30, 40, 50};
    }
}
```
A shorter way to do this:
```cs
class Program
{
    static void Main(string[] args)
    {
        int[] scores = {10, 20, 30, 40, 50};
    }
}
```

## Accessing Array Elements
Elements are accessed using zero-based indexing, meaning the first element has index 0:
```cs
class Program
{
    static void Main(string[] args)
    {
        int[] scores = {10, 20, 30, 40, 50};
        Console.WriteLine(scores[1]); // 20
    }
}
```
## Modifying Array Elements
We can modify array elements as shown:
```cs
class Program
{
    static void Main(string[] args)
    {
        int[] scores = {10, 20, 30, 40, 50};
        Console.WriteLine(scores[1]); // 20
        scores[1] = 90;
        Console.WriteLine(scores[1]); // 90
    }
}
```

## Length of an array
You can get the number of elements in an array using the `Length` property, i.e `array.Length`:
```cs
class Program
{
    static void Main(string[] args)
    {
        int[] scores = {10, 20, 30, 40, 50};
        
        for (var i = 0; i < scores.Length; i++)
        {
            Console.WriteLine(scores[i]);
        }
    }
}
```

## Looping over an array using `foreach`
```cs
class Program
{
    static void Main(string[] args)
    {
        int[] scores = {10, 20, 30, 40, 50};
        
        foreach (int score in scores)
        {
            Console.WriteLine(score);
        }
    }
}
```
Note: you cannot modify array elements inside a `foreach`.