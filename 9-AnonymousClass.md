 * Very similar like Java

```
  abstract class Animal {
    def eat: Unit
  }

  // anonymous class
  val funnyAnimal: Animal = new Animal {
    override def eat: Unit = println("ahahahahahaah")
  }
```

* We can instantiate abstract or non-abstract data types as well.