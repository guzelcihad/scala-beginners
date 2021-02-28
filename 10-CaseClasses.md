* Implements equals, hashcode, toString by default
Useful for especially collections.

* we dont need to use new keyword when instantiating case class. 
 
* Serilazable. Means that best fit for distributed systems. For ex: Akka

* Campanion objects
<br>A companion object is an object that’s declared in the same file as a class, and has the same name as the class
<br>A companion object and its class can access each other’s private members
<br>A companion object’s apply method lets you create new instances of a class without using the new keyword

```
val bob = Person("Bob", 26) //no need to use new 
```

* Class parameters are fields in this type of class.   

```
case class Person(name: String, age: Int)

  // 1. class parameters are fields
  val jim = new Person("Jim", 34)
  println(jim.name)
```

```
  // 4. CCs have handy copy method
  val jim3 = jim.copy(age = 45)
  println(jim3)
```

```
  // 7. CCs have extractor patterns = CCs can be used in PATTERN MATCHING

  case object UnitedKingdom {
    def name: String = "The UK of GB and NI"
  }
```