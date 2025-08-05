# Data Types and Variables

A variable is a named storage location in memory, you use it to store data so you can do something with it later.

A data type tells the computer what kind of data a variable holds.

C# is statitcally typed which means you must declare the data type up front.

To create a variable, specify the type and assign it a value::

`data_type variable_name = value;`

You can also declare a variable and then initialize it later:

`data_type my_var;`

`my_var = value;`

The following variable stores a number:

```cs
int age = 35;
```
- `int` - data type.
- `age` - variable name.
- `35` - value.

## C# Data Types
A data type specifies the size and type of variable values.

It is important to use the correct data type for the corresponding variable, this helps in avoding errors and saving time and memory.

C# has the following data types:

- `int` - 4 bytes - stores whole numbers from -2,147,483,648 to 2,147,483,647.
- `long` - 8 bytes - Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
- `float` - 4 bytes - stores fractional numbers. Sufficient for storing 6 to 7 decimal digits.
- `double` - 8 bytes - Stores fractional numbers. Sufficient for storing 15 decimal digits.
- `bool` - 1 byte - stores either `true` or `false`.
- `char` - 1 byte - stores a single character/letter surrounded by single quotes.
- `string` - 2 bytes - stores a sequence of characters surrounded by double quotes.

Note:
- When using the `long` data type, you should end the value with 'L'.
- When using the `float` data type, you should end the value with 'F'.
- When using the `double` data type, you should end the value with 'D'.

```cs
using System;

class Program
{
    static void Main(string[] args)
    {
        int age = 35;
        long myLong = 150000000000000L;
        float factor = 3.5F;
        double factor2 = 3.29348D;
        bool isMale = true;
        bool isFemale = false;
        string name = "John Doe";
        char grade = 'A';

        Console.WriteLine(age);
        Console.WriteLine(myLong);
        Console.WriteLine(factor);
        Console.WriteLine(factor2);
        Console.WriteLine(isMale);
        Console.WriteLine(isFemale);
        Console.WriteLine(name);
        Console.WriteLine(grade);
    }
}
```

## Variable Naming Rules
- Must start with a letter or an underscore.
- Can't contain spaces or symbols (except `_`).
- C# is case sensitive - `Name` and `name` are not equal.
- Naming convention: **camelCase** for variables and **PascalCase** for constants.