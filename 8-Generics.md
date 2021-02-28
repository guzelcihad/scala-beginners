* Object can not be parameterized
* We can define as many types as we want


# Variance problem
* if B extends A, should List[B] extend List[A]?
  
 ``` 
  //yes (covariant) 
  trait List[+A]
```
```
  //no (invariant) default
  trail List[A]
```

``` 
  // hell no (contravariant)
  trait List[-A]
```

Examples
 ``` 
  // 1. yes, List[Cat] extends List[Animal] = COVARIANCE
  class CovariantList[+A]
  val animal: Animal = new Cat
  val animalList: CovariantList[Animal] = new CovariantList[Cat]
 ``` 

``` 
   // 2. NO = INVARIANCE
  class InvariantList[A]
  val invariantAnimalList: InvariantList[Animal] = new InvariantList[Animal]
``` 

```   
  // 3. Hell, no! CONTRAVARIANCE
  class Trainer[-A]
  val trainer: Trainer[Cat] = new Trainer[Animal]
``` 

# Bounded Types

```
class Car
class SuperCar extends Car
class Garage[T <: Car](Car: T)  //Means T type is subtype of Car