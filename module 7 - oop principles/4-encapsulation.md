# Encapsulation
Encapsulation is the practice of bundling data (fields) and the methods that operate on that data into a single unit, usually a classx, and restricting direct access to some of the object's components.

Encapsulation is about:
- Protecting internal state
- Exposing only what is necessary.
- Preventing unauthorized or invalid changes.

## Achieving encapsulation in C#
- Use access modifiers - `private`, `public`, `protected`.
- properties - expose data via getters and setters.

## Using Access Modifiers
```cs
class BankAccount
{
    private decimal balance = 0;

    public void Deposit(decimal amount)
    {
        if (amount > 0)
        {
            balance += amount;
        }
    }

    public void Withdraw(decimal amount)
    {
        if (amount > 0 && amount <= balance)
        {
            balance -= amount;
        }
    }

    public decimal GetBalance()
    {
        return balance;
    }
}
```

## Properties - the C# way
Instead of `GetBalance()`, you can use a property:

```cs
class BankAccount
{
    private decimal balance;

    public decimal Balance
    {
        get { return balance; }
        private set
        {
            if (value >= 0)
                balance = value;
        }
    }

    public void Deposit(decimal amount)
    {
        if (amount > 0)
            Balance += amount;
    }

    public void Withdraw(decimal amount)
    {
        if (amount > 0 && amount <= Balance)
            Balance -= amount;
    }
}
```

Or even better, with auto-properties (when you don't need much logic):

```cs
public class Person
{
    public string Name { get; set; }  // public get/set
    public int Age { get; private set; }  // only modifiable inside class
}
```
