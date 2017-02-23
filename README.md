# Static  keyword

####We first noticed it in the Main method's declaration:
```C#
static void Main(string[] args)
```
####Class members (variables, properties, methods) can also be declared as static. This makes those members belong to the class itself, instead of belonging to individual objects. No matter how many objects of the class are created, there is only one copy of the static member.
####For example:
```C#
class Cat {
  public static int count=0;
  public Cat() {
    count++;
  }
}
```

####In this case, we declared a public member variable count, which is static. The constructor of the class increments the count variable by one.
####No matter how many Cat objects are instantiated, there is always only one count variable that belongs to the Cat class because it was declared static.

####The same concept applies to static methods. 
####For example:
```C#
class Dog
{
  public static void Bark() {
    Console.WriteLine("Woof");
  }
}
static void Main(string[] args)
{
  Dog.Bark();
}
// Outputs "Woof"
```
####Static methods can access only static members. 
###The Main method is static, as it is the starting point of any program. Therefore any method called directly from Main had to be static.


####Constant members are static by definition.
####For example:
```C#
class MathClass {
  public const int ONE = 1;
}
static void Main(string[] args) {
  Console.Write(MathClass.ONE);
}
//Outputs 1
```

####As you can see, we access the property ONE using the name of the class, just like a static member. This is because all const members are static by default.

####<b>Constructors</b> can be declared static to initialize static members of the class.
The static constructor is automatically called once when we access a static member of the class.
####For example:
```C#
class SomeClass {
  public static int X { get; set; }
  public static int Y { get; set; }
 
  static SomeClass() {
    X = 10;
    Y = 20;
  }
}
```
####The constructor will get called once when we try to access SomeClass.X or SomeClass.Y.

####A static class can contain only static members. 
####We cannot instantiate an object of a static class, as only one instance of the static class can exist in a program.
Static classes are useful for combining logical properties and methods. A good example of this is the<b> Math class</b>.
It contains various useful properties and methods for mathematical operations. 
####For example, the Pow method raises a number to a power:
```C#
Console.WriteLine(Math.Pow(2, 3));
//Outputs 8
```
#### We access all members of the Math class using the class name, without declaring an object.
