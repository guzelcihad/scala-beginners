*  We want to work with functions
pass functions as parameters and use functions as values

* Problem: Scala works on top of the JVM
designed for Java. 
first class elements are objects:

* Solution: All Scala functions are objects.
* Function traits , up to 22 params
* Syntatic sugar function types available


```
trait Function1[-A, +B] {
    def apply(element: A): B
}

Function2[Int, String, Int] //means that takes int and string, returns int
We can write above code like this. (Int, String) => Int  //Syntatic sugar
```

# Code Examples
```
  val doubler = new MyFunction[Int, Int] {
    override def apply(element: Int): Int = element * 2
  }

  println(doubler(2))
```


```
  // function types = Function1[A, B]
  val stringToIntConverter = new Function1[String, Int] {
    override def apply(string: String): Int = string.toInt
  }

  println(stringToIntConverter("3") + 4)
```

```
  val adder: ((Int, Int) => Int) = new Function2[Int, Int, Int] {
    override def apply(a: Int, b: Int): Int = a + b
  }
```

```
//define a function which takes an int and returns another function which takes an int and returns an int

  // Function1[Int, Function1[Int, Int]]
  val superAdder: Function1[Int, Function1[Int, Int]] = new Function1[Int, Function1[Int, Int]] {
    override def apply(x: Int): Function1[Int, Int] = new Function1[Int, Int] {
      override def apply(y: Int): Int = x + y
    }
  }

  val adder3 = superAdder(3)
  println(adder3(4))
  println(superAdder(3)(4)) // curried function
```