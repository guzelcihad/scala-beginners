Scala has single class inheritance.

protected modifiers allows only use in subclasses.
access modifiers => private, protected and public(not declare it)

```
  // constructors
  class Person(name: String, age: Int) {
    def this(name: String) = this(name, 0)
  }
  class Adult(name: String, age: Int, idCard: String) extends Person(name)
```

  we have to define parameters when we extend the class. Its jvm rule, first call super class constructor

  //overriding
  use override keyword at the beginning of the method
  we can also override the vals.

  we can override fields from superclass directly in the class definition.
```
// overriding
class Dog(override val creatureType: String) extends Animal {
//    override val creatureType = "domestic"
    override def eat = {
      super.eat
      println("crunch, crunch")
    }
  }
  ```

```
    // type substitution (broad: polymorphism)
  val unknownAnimal: Animal = new Dog("K9")
  unknownAnimal.eat
```

final method and final class are the same as java.
sealed class allows extension on only the same file. use with sealed keyword.