# Empty constructor generator

A simple C# source generator that generates an empty constructor for a class if it is marked with the EmptyConstructor.EmptyConstructorAttribute attribute.

```csharp
using EmptyConstructor;

[EmptyConstructor]
public partial class ClassName()
{
    private string _name { get; set;}
    public ClassName(string name)
    {
        this._name = name;
    }
}
```

Generates

```csharp
using EmptyConstructor;

[EmptyConstructor]
partial class ClassName()
{
    public ClassName()
    {
    }
}
```

It does nothing if the class already has an empty constructor.
