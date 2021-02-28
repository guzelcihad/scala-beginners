* class Person(name: String) this means that name the visibility of the field name is very restricted. <br>
Scala doesn't generate accessor or mutators. When we add val only getters, adding var getters and setters.
But exceptional case is case classses. Case class constructors parameters are val by default. You don't have
to explicitly define val.


* A companion object is an object that’s declared in the same file as a class, and has the same name as the class
* A companion object and its class can access each other’s private members
* A companion object’s apply method lets you create new instances of a class without using the new keyword
* A companion object’s unapply method lets you de-construct an instance of a class into its individual components