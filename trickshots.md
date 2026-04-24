1. What is the output and why?
```csharp
class Person
{
    public string Name;
}

static void Change(Person p)
{
    p.Name = "Bob";
    p = new Person { Name = "Charlie" };
}

var p1 = new Person { Name = "Alice" };
Change(p1);

Console.WriteLine(p1.Name);
```
