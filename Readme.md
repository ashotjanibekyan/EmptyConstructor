# Empty constructor generator

A simple C# source generator that generates an empty construcotr for a class if it is marked with the EmptyConstructor.GenerateEmptyConstructorAttribute attribute.

```csharp
using EmptyConstructor;

[EmptyConstructorGenerator]
public partial class ClassName()
{
    private string _name { get; set;}
    public ClassName(string name)
    {
        this._name = name;
    }
}
```