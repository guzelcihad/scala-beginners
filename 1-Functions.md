# Scala Functions

When you need loops, use recursion. This is functional programming style.

Its ok to not specify function return type unless u use recursive function.
But its a bad practice

```
def aFunction(a: String, b: Int): String = {
    a + " " + b
}
```

```
def aFunction(a: String, b: Int): String = a + " " + b
```

```
// Function with side effects. Meaning functions can return Unit  
def aFunctionWithSideEffects(aString: String): Unit = println(aString)
```
```
// Also use codeblock in function to define another function
def aBigFunction(n: Int): Int = {
  def aSmallerFunction(a: Int, b: Int): Int = a + b
    aSmallerFunction(n, n-1)
}
```

Call By Value
value is computed before call
same value used everywhere

```
def myFunction(x: Int) : String = ...
val y = myFunction(2)
```

Call By Name
expression is passed literally
expression is evaluated at every use within

```
def myFunction(x: => Int) : String = ...
val y = myFunction(2)
```

Default and Named Arguments
Similar to Python style not in Java.

```
def savePicture(format: String = "jpg", width: Int = 1920, height: Int = 1080): Unit = println("saving picture")

  /*
    1. pass in every leading argument
    2. name the arguments
   */
  
  savePicture(height = 600, width = 800, format = "bmp")
```