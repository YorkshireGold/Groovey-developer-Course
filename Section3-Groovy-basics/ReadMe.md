### Assertions
```
// you must provide an assertion an expression that evaluates to true
assert true

// we can provide a full expression on the right hand side 
// note that unlike Java and more like Ruby or Scala == is equality 
assert 1 == 1

// like the example above we are evaluating an expression
def x = 1
assert x == 1

// what happens when the expression doesn't evaluate to true? 
assert false

// The power assertion output shows evaluation results from the outer to the inner expression
assert 1 == 2

// complex debug output
assert 1 == (3 + 10) * 100 / 5 * 20

// The power assertion statements true power unleashes in complex Boolean statements, 
// or statements with collections or other toString-enabled classes:
def x = [1,2,3,4,5]
assert (x << 6) == [6,7,8,9,10]

```

### scripts and Classes

Groovy has two ways to treat a `.groovy` file. Its either a script or a class definition. If it's a script the script cannot contain a class definition as the same name as the file. If you were working in Java file, you need to have a class of hte same name. In Groovy you don't. 

```

// a script is any groovy code not enclosed in a class file
// but don't make the mistake thinking there is no class
println "Hello from myscript.groovy"

```

If you create a class you would need to have the same name as the classname in the class file. The convention is to name classes with a CAPITAL letter.

### Numbers

In Java when you create a variable with a primitive types , you cannot invoke methods on them because they are primitive types, not objects. 

### Annotations and AST transformations

Annotations are ways to communicate with the compiler. For example at he top of a class you might put `@Controller`. This will define to the compiler that the particular set of code is a controller. Upi can event pass these arguments eg `@Controller(name="MyHomeController)`. for the most part we will be the consumers of controllers , but you cna make your own ones; but thats not for beginners. Unlike the Java Annotations. they can be used to alter the semantics of a language. Another example is the AST transformation Annotation. 

### Grapes

Grape is a jar dependency manager embedded into groovy. Grape lets you quicky add Maven dependencies to you class path which makes scripting much easier.

"http://docs.groovy-lang.org/latest/html/documentation/grape.html"

We use the `@Grab()` annotation to pull in a dependency library and here is where they can be found. 

`@Grab(group='org.springframework', module='spring-orm', version='3.2.5.RELEASE')`
`@Grab('org.springframework:spring-orm:3.2.5.RELEASE')`