## Adding Comment Line

```ruby
/**
 * This is one type of comment Line
 */

// This is the another type of comment line
```


## Calling Variables, Functions from Another Class and String Interpolation

```ruby
fun main(args: Array<String>) {

    var personObj = Person()
    personObj.name = "Steve"

    println("The name of the person is ${personObj.name}") // String Interpolation
    
    personObj.details("Jhon")
}

class Person {

    var name: String = ""
    
    fun details(mValue: String){
         println("The name of the person is " + mValue) // String Append
    }
}
```  

## By Using Constrcutor

```ruby
fun main(args: Array<String>) {

    var personObj = Person("Steve")
    personObj.details()
  
}

class Person(var mValue: String) {

    fun details(){
         println("The name of the person is " + mValue)
    }
}
```

## Ranges  

```ruby
fun main() {	

    val mValue0 = 1..5 // Range from 1 to 5
    val mValue1 = 5 downTo 1 // Descending the value from 5 to 1
    val mValue2 = 1..5 step 2 // Contains the value 1,3,5
    val mValue3 = 5 downTo 1 step 2 // Contains the value 5,3,1
    val mValue4 = 19.downTo(1) // Contains the value from 19 to 1
    val mValue5 = 1.rangeTo(5) // Contains the value from 1 to 5
    val mValue6 = 'a'..'z' // Characters from a to z
    
    val mValue7 = 5 in mValue1 // 5 is present in 5..1
    
   for (i in mValue2) {
        println(i)
    }
   
   println(mValue6)
   
}
```  

## If as Expression  

```ruby
fun main(args: Array<String>) {

    val a = 5

    val b = 10

    var maxValue: Int = if (a > b) {
                            println("a is greater")
                            a // Last statement will be executed if we are having multiple lines of Code.
                        } else {
                            println("b is greater")
                            b
                        }

    println(maxValue)
}
```

## Need to Know

- REPL - Read-Eval-Print-Loop ( Tools -> Kotlin -> Kotlin REPL )
- Iterators - For Loop, While and doWhile Loop.
- Iterators - Loop Control Statements (Break Statement, Continue Statement and Return Statement)
- Statically Typed - Data type must be defined.
- Labeled For Loop - @myLoop to reflect in the Outer For Loop.
- Unit - Void in Java.
- String Interpolation - “The sum is ${a+b}”.
- Primitive DataType - boolean, char, byte, short, int, long, float and double.
- Non Primitive DataType - classes, Strings, Interfaces and Arrays.
