* Its still object oriented . How to solve this? Use lambda



```
  // anonymous function (LAMBDA)
  val doubler: Int => Int = (x: Int) => x * 2

  // multiple params in a lambda
  val adder: (Int, Int) => Int = (a: Int, b: Int) => a + b

  // no params
  val justDoSomething: () => Int = () => 3

  // careful use () with lambda.
  println(justDoSomething) // function itself
  println(justDoSomething()) // call

  // curly braces with lambdas. Not recommended
  val stringToInt = { (str: String) =>
    str.toInt
  }
```

* Syntatic sugar
```
  // MOAR syntactic sugar
  val niceIncrementer: Int => Int = _ + 1 // equivalent to x => x + 1
  val niceAdder: (Int, Int) => Int = _ + _ // equivalent to (a,b) => a + b
```