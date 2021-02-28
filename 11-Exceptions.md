* Throwing an exception return Nothing

```
    val aWeirdValue: String = throw new NullPointerException
```    

* Catching an exception

```
  def getInt(withExceptions: Boolean): Int =
    if (withExceptions) throw new RuntimeException("No int for you!")
    else 42
    
  val potentialFail = try {
    // code that might throw
    getInt(false)
  } catch {
    case e: RuntimeException => 43
  } finally {
    // code that will get executed NO MATTER WHAT
    // optional
    // does not influence the return type of this expression
    // use finally only for side effects
    println("finally")
  }
```