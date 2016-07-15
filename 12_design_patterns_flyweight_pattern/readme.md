# Design Patterns - Flyweight Pattern

[Flyweight pattern](http://www.tutorialspoint.com/design_pattern/flyweight_pattern.htm) is primarily used to reduce the number of objects created and to decrease memory footprint and increase performance. This type of design pattern comes under structural pattern as this pattern provides ways to decrease object count thus improving the object structure of application.

Flyweight pattern tries to reuse already existing similar kind objects by storing them and creates new object when no matching object is found. We will demonstrate this pattern by drawing 20 circles of different locations but we will create only 5 objects. Only 5 colors are available so color property is used to check already existing Circle objects.

Note: origial tutorial gives the following warnings:
```
.\ShapeFactory.java:4: warning: [rawtypes] found raw type: HashMap
   private static final HashMap<String, Shape> circleMap = new HashMap();
                                                               ^
  missing type arguments for generic class HashMap<K,V>
  where K,V are type-variables:
    K extends Object declared in class HashMap
    V extends Object declared in class HashMap
.\ShapeFactory.java:4: warning: [unchecked] unchecked conversion
   private static final HashMap<String, Shape> circleMap = new HashMap();
                                                           ^
  required: HashMap<String,Shape>
  found:    HashMap
2 warnings
```

To remove the error:

* Replace 
```
private static final HashMap<String, Shape> circleMap = new HashMap();
```

* With
```
private static final HashMap<String, Shape> circleMap = new HashMap<String, Shape>();
```


## Build

javac -cp . -Xlint:all FlyweightPatternDemo.java

## Run

java FlyweightPatternDemo