# `this` keyword
The this keyword refers to the current instance of the class, the specific object that’s executing the code.

```cs
class Person
{
    public string FirstName;
    public string LastName;

    public Person(string firstName, string lastName)
    {
        this.FirstName = firstName;
        this.LastName = lastName;
    }

    public void greet()
    {
        Console.WriteLine($"Hello, my name is {this.FirstName} {this.LastName}");
    }
}
```