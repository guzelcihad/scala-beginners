# Abstract Classes

We dont have to use override in subclasses to implement Abstract Class methods or fields.

The definition

```
  abstract class Animal {
    val creatureType: String = "wild"
    def eat: Unit
  }
```

Concrete class sample
```
  class Dog extends Animal {
    override val creatureType: String = "Canine"
    def eat: Unit = println("crunch crunch")
  }
```

# TRAITS
* It looks similar to interface in java.
```
  trait Carnivore {
    def eat(animal: Animal): Unit
    val preferredMeal: String = "fresh meat"
  }
```

* We can implement more than one traits like this
```
class Crocodile extends Animal with Carnivore with ColdBlooded {# TRAITS
```

 * traits vs abstract classes
  // 1 - traits do not have constructor parameters  => trait Carnivore(val name) not allowed
  // 2 - multiple traits may be  inherited by the same class
  // 3 - traits = behavior, abstract class = "thing"
  // We can define concrete and abstract method in trait

# SCALA TYPE HIERARCHY
                                scala.Any
    scala.AnyVal(for primitive types)                scala.AnyRef
    Int, Unit, Boolean                               String, List, Set...       

                                                    scala.Null
                    scala.Nothing