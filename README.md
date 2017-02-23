# Static  keyword

####We first noticed it in the Main method's declaration:
```C#
static void Main(string[] args)
```
Class members (variables, properties, methods) can also be declared as static. This makes those members belong to the class itself, instead of belonging to individual objects. No matter how many objects of the class are created, there is only one copy of the static member.
For example:
```C#
class Cat {
  public static int count=0;
  public Cat() {
    count++;
  }
}
```

In this case, we declared a public member variable count, which is static. The constructor of the class increments the count variable by one.
No matter how many Cat objects are instantiated, there is always only one count variable that belongs to the Cat class because it was declared static.
