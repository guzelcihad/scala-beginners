lets define a class;

```
class Person(name: String, age: Int)

val person = new Person("John", 26) //instantiate it
person.age // wrong , we can not do this. Because class parameters are not fields.
```

```
class Person(name: String, val age: Int)
person.age //valid
```

class parameters and class fields are two different things.

---------------
```
  // constructor
  class Person(name: String, val age: Int = 0) {
    // body
    val x = 2

    println(1 + 3)
  }
```
```
  val person = new Person("John", 26) //instantiate it
  println(person.x)
```

  output
  4
  2

  why? Because first evaluate expression when we instantiate the class
  then print x value.

  Note here: println() is allowed in class inside because remember this is called
  block expression in scala. We can not allowed to make it in Java.

  The value x is a field in this case.

  Overloading is the same concept like Java.
  And usage of this keyword is same.
     // method

```
    def greet(name: String): Unit = println(s"${this.name} says: Hi, $name")

    // overloading
    def greet(): Unit = println(s"Hi, I am $name")
```

NOTES
defining class 
```
class Person(name: String, age: Int)
```

instantiating
```
val bob = new Person("Bob", 25)
```
parameters vs fields 

calling method
syntax allowed for parameter-less methods
val bobSayHi = bob.greet