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

2.
```
string a = "hello";
string b = "he" + "llo";
string c = new string("hello".ToCharArray());

Console.WriteLine(a == c);
Console.WriteLine(object.ReferenceEquals(a, c));
Console.WriteLine(a.Equals(c));
Console.WriteLine(object.ReferenceEquals(a, b));
```

```
int x = 5;
object o = x;

x++;
Console.WriteLine(o);
```

```
string x = "Hello";
Modify(x);

Console.WriteLine(x);
```

```
string[] arr = new string[1];
object[] objs = arr;

objs[0] = 123;
```

```
class Base
{
    public virtual void Foo()
    {
        Bar();
    }

    public virtual void Bar()
    {
        Console.WriteLine("Base Bar");
    }
}

class Derived : Base
{
    public override void Foo()
    {
        base.Foo();
    }

    public override void Bar()
    {
        Console.WriteLine("Derived Bar");
    }
}

Base x = new Derived();
x.Foo();
```

