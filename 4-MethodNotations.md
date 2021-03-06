  ```
  val mary = new Person("Mary", "Inception")
  println(mary.likes("Inception"))
  println(mary likes "Inception") // equivalent
  // infix notation = operator notation (syntactic sugar also its called like this)
```

  those two methods call are the same. its called infix notation or operator notation
  only apply for which methods have one parameter.

  we can also name method as such mathematical operations like +, -, / 
  scala allows us to do that freedom.

```
// "operators" in Scala
  val tom = new Person("Tom", "Fight Club")
  println(mary + tom)  
  println(mary.+(tom)) //same with above

println(1 + 2)
println(1.+(2))
```

also those are the same
overall,   // ALL OPERATORS ARE METHODS.

```
  // prefix notation
  val x = -1  // equivalent with 1.unary_-
  val y = 1.unary_-
  // unary_ prefix only works with - + ~ !
```

```
  // postfix notation => only works for methods without parameters
   def isAlive: Boolean = true
  println(mary.isAlive)
  println(mary isAlive)
```

there is a special method name apply in scala.

```
def apply(): String = s"Hi, my name is $name and I like $favoriteMovie"

  // apply
  println(mary.apply())
  println(mary()) // equivalent
```
  