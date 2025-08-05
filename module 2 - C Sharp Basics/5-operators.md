# Operators
In C#, operators help you do everything from math to comparisons to decision-making.

There are the following categories of operators:
- Arithmetic operators
- Relational (comparison) operators
- Logical operators
- Bitwise operators

## Arithmetic Operators
These operators help you do math and are very straightforward.

They include:
- Addition - `+`
- Subtraction - `-`
- Multiplication - `*`
- Division - `/`
- Modulus - `%`
- Increment - `++`
- Decrement - `--`
- Assignment - `=`
- Addition assignment - `+=`
- Subtraction assignment - `-=`
- Multiplication assignment - `*=`
- Division assignment - `/=`
- e.t.c.

```cs
class Program
{
    static void Main(string[] args)
    {
        int a = 10;
        int b = 3;

        Console.WriteLine(a + b);
        Console.WriteLine(a - b);
        Console.WriteLine(a / b);
        Console.WriteLine(a % b);
        Console.WriteLine(a * b);

        a++;
        b++;
        Console.WriteLine(a);
        Console.WriteLine(b);

        a--;
        b--;
        Console.WriteLine(a);
        Console.WriteLine(b);

        a += 5;
        b += 5;
        Console.WriteLine(a);
        Console.WriteLine(b);
    }
}
```

## Relational Operators
They help you compare values, and return `true` or `false`.

They are:
- Equal - `==`
- Not Equal - `!=`
- Greater than - `>`
- Less than - `<`
- Greater or equal - `>=`
- Less or equal - `<=`

```cs
class Program
{
    static void Main(string[] args)
    {
        int a = 10;
        int b = 3;

        Console.WriteLine(a > b);
        Console.WriteLine(a < b);
        Console.WriteLine(a != b);
        Console.WriteLine(a == b);
    }
}
```

## Logical Operators
They let you combine conditions and return `true` or `false`.

They are:
- `&&` - (AND) returns true if both conditions are true.
- `||` - (OR) returns true if either condition is true
` `!` - (NOT) reverses the boolean (true flipped to false and vice versa).

```cs
class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine(true && true);
        Console.WriteLine(true && false);
        Console.WriteLine(true || true);
        Console.WriteLine(true || false);
        Console.WriteLine(false || false);
        Console.WriteLine(!true);
    }
}
```