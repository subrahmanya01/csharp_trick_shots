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
```csharp
string a = "hello";
string b = "he" + "llo";
string c = new string("hello".ToCharArray());

Console.WriteLine(a == c);
Console.WriteLine(object.ReferenceEquals(a, c));
Console.WriteLine(a.Equals(c));
Console.WriteLine(object.ReferenceEquals(a, b));
```
3.
```csharp
int x = 5;
object o = x;

x++;
Console.WriteLine(o);
```

4.
```csharp
string x = "Hello";
Modify(x);

Console.WriteLine(x);
```

5.
```csharp
string[] arr = new string[1];
object[] objs = arr;

objs[0] = 123;
```
6.
```csharp
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
7.
```
class A {}
class B : A {}

A x = new B();

Console.WriteLine(x is A); 
Console.WriteLine(x.GetType() == typeof(A));
```

