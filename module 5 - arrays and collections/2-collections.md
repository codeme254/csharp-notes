# Collections
Collections are classes in the .NET Framework that hold groups of related objects.

Unlike arrays, collections:
- grow/shrink dynamically
- offer advanced operations like searching, sorting and filtering.
- often include type safety

## Types of Collections
These are found in the `System.Collections.Generic` namespace.

They include:
- `List<T>` - a growable, type-safe array.
- `Dictionary<TKey, TValue>` - key value store with fast lookup.
- `HashSet<T>` - unordered, unique items.
- `Queue<T>` - first-in, first-out collection.
- `Stack<T>` - Last-in, first-out collection.
- `LinkedList<T>` - doubly-linked list (fast insert/delete).
- `SortedList<TKey, TValue>` - keeps keys sorted.

## `List<T>`
In C#, the List<T> class represents the list of objects that can be accessed by index.

It comes under the `System.Collections.Generic` namespace.

It is different from the arrays. A List<T> can be resized dynamically but arrays cannot.

### Creating A List
To create a list, follow this syntax:

`List<data_type> name = new List<data_type>()`

Example: a list of strings:

```cs
class Program
{
    static void Main(string[] args)
    {
        List<string> fruits = new List<string>();
    }
}
```
### Adding elements to a list using `list.Add()` Method

```cs
class Program
{
    static void Main(string[] args)
    {
        List<string> fruits = new List<string>();
        fruits.Add("Banana");
        fruits.Add("Mangos");
        fruits.Add("Apples");
        fruits.Add("Cherry");
    }
}
```

### Getting the number of elements in a list
You can get the number of elements in a list using the `Count` property:

```cs
class Program
{
    static void Main(string[] args)
    {
        List<string> fruits = new List<string>();
        fruits.Add("Banana");
        fruits.Add("Mangos");
        fruits.Add("Apples");
        fruits.Add("Cherry");
        Console.WriteLine(fruits.Count); // 4
    }
}
```

### Looping over a list
You can use the for loop or the foreach loop to loop over a list:
```cs
class Program
{
    static void Main(string[] args)
    {
        List<string> fruits = new List<string>();
        fruits.Add("Banana");
        fruits.Add("Mangos");
        fruits.Add("Apples");
        fruits.Add("Cherry");
        
        for (int i = 0; i < fruits.Count; i++)
        {
            Console.WriteLine(fruits[i]);
        }

        foreach(var fruit in fruits)
        {
            Console.WriteLine(fruit);
        }
    }
}
```

### Removing elements from a list
You can use the `Remove` method to remove an element from a list:
```cs
class Program
{
    static void Main(string[] args)
    {
        List<string> fruits = new List<string>();
        fruits.Add("Banana");
        fruits.Add("Mangos");
        fruits.Add("Apples");
        fruits.Add("Cherry");

        fruits.Remove("Mangos");

        foreach(var fruit in fruits)
        {
            Console.WriteLine(fruit);
        }
    }
}
```

### Determining whether an element is in a List
You can use `Contains` to determine whether an element is in a List.

It returns true to mean the element is available and false to mean the element is not available.

```cs
class Program
{
    static void Main(string[] args)
    {
        List<string> fruits = new List<string>();
        fruits.Add("Banana");
        fruits.Add("Mangos");
        fruits.Add("Apples");
        fruits.Add("Cherry");

        Console.WriteLine(fruits.Contains("Mangos")); // true
        Console.WriteLine(fruits.Contains("Pawpaw")); // false

        foreach (var fruit in fruits)
        {
            Console.WriteLine(fruit);
        }
    }
}
```

### Inserting elements at a specific position
You can insert an element into a list at a specific position.

To do this, use the `Insert` method. It takes in two parameters, the first one is the index at which to insert and the second one is the element to insert:
```cs
class Program
{
    static void Main(string[] args)
    {
        List<string> fruits = new List<string>();
        fruits.Add("Banana");
        fruits.Add("Mangos");
        fruits.Add("Apples");
        fruits.Add("Cherry");

        fruits.Insert(1, "Pawpaw");

        foreach (var fruit in fruits)
        {
            Console.WriteLine(fruit);
        }
    }
}
```

### Remove all elements from a list
To remove all elements from a list, use the `Clear` method:
```cs
class Program
{
    static void Main(string[] args)
    {
        List<string> fruits = new List<string>();
        fruits.Add("Banana");
        fruits.Add("Mangos");
        fruits.Add("Apples");
        fruits.Add("Cherry");

        fruits.Clear();

        foreach (var fruit in fruits)
        {
            Console.WriteLine(fruit);
        }
    }
}
```
[Learn more about lists](https://www.geeksforgeeks.org/c-sharp/c-sharp-list-class/)

## `Dictionary<TKey, TValue>`
Dictionary in C# is a generic collection that stores key-value pairs.

A dictionary is defined under `System.Collections.Generic` namespace.

It is dynamic in nature means the size of the dictionary is growing according to the need.

### Creating a Dictionary
To create a dictionary, we follow the syntax:

`Dictionary<KeyType, ValueType> dictionary_name = new Dictionary<KeyType, ValueType>();`

```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
    }
}
```

### Adding key value pairs to a dictionary
You can use the square bracket notation or use the `Add` method
```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
        ages["Alice"] = 22;
        ages["John"] = 48;
        ages.Add("Alison", 30);
        ages.Add("Kennedy", 25);
    }
}
```

### Accessing the values of a dictionary
Use the square bracket notation:
```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
        ages["Alice"] = 22;
        ages["John"] = 48;
        ages.Add("Alison", 30);
        ages.Add("Kennedy", 25);

        Console.WriteLine(ages["Alice"]);
    }
}
```

### Number of key value pairs
You can get the number of key value pairs in a dictionary using the `Count` method:
```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
        ages["Alice"] = 22;
        ages["John"] = 48;
        ages.Add("Alison", 30);
        ages.Add("Kennedy", 25);

        Console.WriteLine(ages.Count); // 4
    }
}
```

### Accessing key value pairs by index
You can access key value pairs using indexes starting from 0:

### Removing a key value pair from a dictionary
Use the `Remove` method to remove a key value pair, pass the key to the method.

```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
        ages["Alice"] = 22;
        ages["John"] = 48;
        ages.Add("Alison", 30);
        ages.Add("Kennedy", 25);

        ages.Remove("Kennedy");

        Console.WriteLine(ages.Count); // 3
    }
}
```

### Check whether a dictionary contains a specified key
Use the `ContainsKey` method to check whether a dictionary contains the specified key:
```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
        ages["Alice"] = 22;
        ages["John"] = 48;
        ages.Add("Alison", 30);
        ages.Add("Kennedy", 25);

        Console.WriteLine(ages.ContainsKey("Alison")); // true
        Console.WriteLine(ages.ContainsKey("Doe")); // false

        Console.WriteLine(ages.Count);
    }
}
```

### Check whether a dictionary contains a specified value
Use the `ContainsValue` method to check whether a dictionary contains a specified value:

```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
        ages["Alice"] = 22;
        ages["John"] = 48;
        ages.Add("Alison", 30);
        ages.Add("Kennedy", 25);

        Console.WriteLine(ages.ContainsValue(22)); // true
        Console.WriteLine(ages.ContainsValue(1000)); // false

        Console.WriteLine(ages.Count);
    }
}
```

### Remove all key value pairs
Use the `Clear` method to remove all the key value pairs of a dictionary.

```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
        ages["Alice"] = 22;
        ages["John"] = 48;
        ages.Add("Alison", 30);
        ages.Add("Kennedy", 25);

        ages.Clear();

        Console.WriteLine(ages.Count); // 0
    }
}
```

### Looping through a dictionary
```cs
class Program
{
    static void Main(string[] args)
    {
        Dictionary<string, int> ages = new Dictionary<string, int>();
        ages["Alice"] = 22;
        ages["John"] = 48;
        ages.Add("Alison", 30);
        ages.Add("Kennedy", 25);

        foreach(KeyValuePair<string, int> entry in ages)
        {
            Console.WriteLine($"{entry.Key} - {entry.Value}");
        }
    }
}
```