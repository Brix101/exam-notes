# Class:

- A class is a blueprint or template for creating objects.
- It defines a set of attributes (properties) and methods (functions) that the objects created from the class will have.

Example (in C#):

```csharp
public class Car
{
    // Attributes
    public string Model;
    public string Color;

    // Methods
    public void Start()
    {
        Console.WriteLine("The car is starting.");
    }

    public void Drive()
    {
        Console.WriteLine("The car is moving.");
    }
}
```

### Object:

- An object is an instance of a class. It represents a real-world entity and is created based on the class definition.

Example (in C#):

```csharp
// Creating an instance of the Car class
Car myCar = new Car();

// Setting attributes
myCar.Model = "Toyota";
myCar.Color = "Blue";

// Calling methods
myCar.Start();
myCar.Drive();
```

### Inheritance:

- Inheritance allows a class (subclass/derived class) to inherit attributes and methods from another class (superclass/base class).
- It promotes code reuse and the creation of a hierarchy of classes.

Example (in C#):

```csharp
// Base class
public class Vehicle
{
    public string Type;

    public void Move()
    {
        Console.WriteLine("The vehicle is moving.");
    }
}

// Derived class inheriting from Vehicle
public class Car : Vehicle
{
    public string Model;
}
```

### Encapsulation:

- Encapsulation is the bundling of data (attributes) and methods that operate on the data into a single unit (class).
- It hides the internal details of the object and allows access to the object's functionality through a well-defined interface.

Example (in C#):

```csharp
public class BankAccount
{
    private decimal balance; // Encapsulated attribute

    // Encapsulated method to access the balance
    public decimal GetBalance()
    {
        return balance;
    }

    // Encapsulated method to update the balance
    public void Deposit(decimal amount)
    {
        balance += amount;
    }
}
```

### Polymorphism:

- Polymorphism allows objects of different types to be treated as objects of a common type.
- It can be achieved through method overloading or method overriding.

Example (in C#):

```csharp

// Base class
public class Shape
{
    public virtual void Draw()
    {
        Console.WriteLine("Drawing a shape");
    }
}

// Derived classes with overridden methods
public class Circle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle");
    }
}

public class Square : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a square");
    }
}
```

These are the basic concepts of OOP. Understanding and practicing these concepts will help you structure your code in a more organized and reusable way.
