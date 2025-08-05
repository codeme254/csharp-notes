# Type Inference
Type inference in C# means letting the compiler figure out the data type for you based on the what value has been assigned initially.

Type inference in C# is achieved using the `var` keyword.
```cs
class Program
{
    enum Role
    {
        Admin,
        Editor,
        Reader
    }
    static void Main(string[] args)
    {
        var name = "Dennis";
        var age = 35;
        var role = Role.Admin;
        var isFemale = false;

        Console.WriteLine(name);
        Console.WriteLine(age);
        Console.WriteLine(role);
        Console.WriteLine(isFemale);
    }
}
```

## You Must Initialize `var`
`var` must always be initialized.

This will not work:
```cs
var age;
age = 35;
```

But this will:
```cs
var age = 35;
```