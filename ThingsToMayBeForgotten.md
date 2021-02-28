* class Person(name: String) this means that name the visibility of the field name is very restricted. <br>
Scala doesn't generate accessor or mutators. When we add val only getters, adding var getters and setters.
But exceptional case is case classses. Case class constructors parameters are val by default. You don't have
to explicitly define val.