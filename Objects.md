
```
// SCALA DOES NOT HAVE CLASS-LEVEL FUNCTIONALITY ("static")
  object Person { // type + its only instance
    // "static"/"class" - level functionality
    val N_EYES = 2
    def canFly: Boolean = false
```

we can access those var or function like that : Person.N_EYES or Person.canFly
we can define val, var or function inside object in scala.

Scala objects are singleton instances. For ex: Person object above

```
    // Scala object = SINGLETON INSTANCE
    val mary = Person
    val john = Person
    println(mary == john)  //true
```

if we have object and class with the same name in the same block, its called COMPANIONS.

FACTORY METHODS
defines in objects. Actually they are apply methods mention earlier.

```
    // factory method
    def apply(mother: Person, father: Person): Person = new Person("Bobbie")

    then we can use =>    val bobbie = Person(mary, john)

  // Scala Applications = Scala object with
  // def main(args: Array[String]): Unit
```  

  this is the same as java main method. 

TAKEAWAYS
scala doesn't have static values / methods.
Scala has objects. 