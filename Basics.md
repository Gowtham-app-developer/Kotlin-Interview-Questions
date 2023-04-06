# Kotlin-Basics

## Table of Contents

| S.No | Content |
| --------	 | ------------ |
| 1 | [Adding Comment Line](Basics.md#adding-comment-line) |  
| 2 | [Declaring Variables](Basics.md#declaring-variables) |  
| 3 | [Declaring Variables and Methods](Basics.md#declaring-variables-and-methods) |  
| 4 | [String Interpolation](Basics.md#string-interpolation) |  
| 5 | [Calling Variables & Functions](Basics.md#calling-variables--functions-from-another-class) |
| 6 | [By Using Primary Constrcutor](Basics.md#by-using-primary-constrcutor) |
| 7 | [Ranges](Basics.md#ranges) |
| 8 | [If as Expression](Basics.md#if-as-expression) |
| 9 | [For Loop](Basics.md#for-loop) |
| 10 | [While Loop](Basics.md#while-loop) |
| 11 | [do While Loop](Basics.md#do-while-loop) |
| 12 | [Break Statement with Labeled For Loop](Basics.md#break-statement-with-labeled-for-loop) |
| 13 | [Continue Statement with Labeled For Loop](Basics.md#continue-statement-with-labeled-for-loop) |
| 14 | [Function with Return Type](Basics.md#function-with-return-type) |
| 15 | [Function as Expression](Basics.md#function-as-expression) |
| 16 | [Default Function Parameters](Basics.md#default-function-parameters) |
| 17 | [Named Parameters](Basics.md#named-parameters) |
| 18 | [Null Safety Operators](Basics.md#null-safety-operators) |  
| 19 | [Lateinit Keyword](Basics.md#lateinit-keyword) |  
| 20 | [Lazy Initialization](Basics.md#lazy-initialization) |
| 21 | [Need to Know](Basics.md#need-to-know) |

## Adding Comment Line

- A comment is an explanation or description of the source code of the program.
- Generally Comment makes the program easier to read and understand.
- These are the statements that are not executed by the compiler or an interpreter.
- Type -> Single Line Comment, Multiple Line Comment.

__Example__

```ruby
// TODO - This is the Single Line Comment.
```

```ruby
/**
 * TODO - This is the Multiple Line Comment.
 */
```
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

## Declaring Variables

__Eample__

```ruby
fun main() {

    private var mStringValueOne: String = "One" // TODO Declaring a Value in the mutable string explicitly using var.
    
    private var mStringValueTwo = "ValueTwo" // TODO Declaring a Value in the mutable string implicitly using var.

    private var mStringValueThree: String? = null // TODO Declaring the null value in the mutable string explicitly using var.

    private lateinit var mStringValueFour: String // TODO Later We can Assign a Value using lateinit Keyword using var.

    private val mStringValueFive: String = "Four" // TODO Declaring a Value in the immutable string explicitly using val.

    private val mStringValueSix: String by lazy { "Five" } // TODO Declaring a Value in the immutable string explicitly using val by lazy keyword.
    
    private var mStringValueSeven: String? = null // TODO Declaring a Null Value in the mutable string explicitly using var.
    
    private val mStringValueSeven: String? = null // TODO Declaring a Null Value in the mutable string explicitly using val.
    
    println(mStringValueOne)

}    
```  

:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  


## Declaring Variables and Methods  

```ruby
fun main(args: Array<String>) {

    lateinit var mString: String // TODO Declaring Mutable String Explicitly
    mString = "Hello World!!!"
    println(mString)

    val mStringOne = "Hello World!!!" // TODO Declaring Immutable String Implicitly
    println(mStringOne)

    mAddTwoValues() // TODO Calling a Method

    println(mAddMultipleValues())  
    
    println(mAddMultipleValues(7,2))
}

fun mAddTwoValues() { // TODO Declaring a Method
    println(1 + 2)
}

fun mAddMultipleValues(): Int { // TODO Declaring a Method with a Return Value
    return 1 + 4
}

fun mAddMultipleValues(mValue1:Int, mValue2:Int): Int { // TODO Declaring a Method with the Parameters
    return mValue1 * mValue2
}
```
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

## String Interpolation

```ruby
fun main() {

  var mValueOne = "Gauthy" 
  var mValueTwo = "World"

  print("Welcome to "+ mValueOne + " " + mValueTwo) // TODO - String Append
  print("Welcome to $mValueOne $mValueTwo") // TODO - String Interpolation
  print("The Length is ${mValueOne.length}") // TODO - String Interpolation
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

## Calling Variables & Functions from Another Class

```ruby
fun main(args: Array<String>) {

    var personObj = Person()
    personObj.name = "Gauthy"

    println("The name of the person is ${personObj.name}") // TODO - String Interpolation
    
    personObj.details("Gowtham")
}

class Person {

    var name: String = ""
    
    fun details(mValue: String){
         println("The name of the person is " + mValue) // TODO - String Append
    }
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## By Using Primary Constrcutor

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
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## Ranges  

```ruby
fun main() {	

    val mValue0 = 1..5 // TODO - Range from 1 to 5
    val mValue1 = 5 downTo 1 // TODO - Descending the value from 5 to 1
    val mValue2 = 1..5 step 2 // TODO - It Contains the value 1,3,5
    val mValue3 = 5 downTo 1 step 2 // TODO - It Contains the value 5,3,1
    val mValue4 = 19.downTo(1) // TODO - It Contains the value from 19 to 1
    val mValue5 = 1.rangeTo(5) // TODO - It Contains the value from 1 to 5
    val mValue6 = 'a'..'z' // TODO - It Characters from a to z
    
    val mValue7 = 5 in mValue1 // TODO - It checks whether the 5 is present in 5..1
    
   for (i in mValue2) { // TODO - By Using for loop, we can iterate over any Iterable such as a range, an array, or a collection.
        println(i)
    }
   
   println(mValue6)
   
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## If as Expression  

```ruby
fun main(args: Array<String>) {

    val a = 5
    val b = 10

    var maxValue: Int = if (a > b) {
                            println("a is greater")
                            a // TODO - Last statement will be executed if we are having multiple lines of Code.
                        } else {
                            println("b is greater")
                            b
                        }

    println(maxValue)
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## For Loop 

```ruby  
// TODO - By using For Loop we will Initialize, check the condition, then print the Statement and finally we Increment.  

fun main(args: Array<String>) {

    for (i in 1..20) { 

        if (i % 2 == 0) {
            println(i)
        }
    }

    for (i in 20 downTo 0) {

        if (i % 2 == 0) {
            println(i)
        }
    }
}
```
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## While Loop 

```ruby  
// TODO - In while Loop we will Initialize, check the condition, then print the Statement and finally we Increment.  

fun main(args: Array<String>) {

    var i = 0 
    
    while (i <= 10) {
        if (i % 2 == 0) {
            println(i)
        }
        i++
    }

    var j = 10
    
    while (j >= 0) {
        if (j % 2 == 0) {
            println(j)
        }
        j--
    }
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## do While Loop 

```ruby  
// TODO In do while Loop we will Initialize, print the Statement, then we Increment and finally we will do the condition check.  

fun main(args: Array<String>) {

    var i = 0

    do {
        if (i % 2 == 0) { 
            println(i)
        }
        i++
    } while (i <= 10)


    var j = 10

    do {
        if (j % 2 == 0) {
            println(j)
        }
        j--
    } while (j >= 0)
}
```
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## Break Statement with Labeled For Loop

__Example_1__

```ruby
fun main(args: Array<String>) {

    for (i in 1..20) { 
            
            println(i)
            
           if(i==5){
              break // TODO When the value becomes 5 then it won't stop further.
           }
    }
}
```

__Example_2__

```ruby
fun main() {	
   
mLoop@ for(i in 1..9){
         for(j in 1..9){
              if(i==2 && j==2)
              break@mLoop // TODO We used Labeled For Loop to reflect the changes in Outer For Loop
            println("$i $j")
         }
    }
 
}
```
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## Continue Statement with Labeled For Loop

```ruby
fun main() {	
   
mLoop@ for(i in 1..9){
         for(j in 1..9){
              if(i==2 && j==2)
              continue@mLoop // TODO When the value become i == 2 and j == 2 it omits the Value and print further.
            println("$i $j")
         }
    }
 
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## Function with Return Type

```ruby
fun main() {	

   println("Sum is ${mAdd(2,3)}")
 
}

fun mAdd(a:Int, b:Int): Int {
    return a+b
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## Function as Expression

```ruby
fun main() {	
  
    var mSum = mCheckCondition (3,4)
    
     print("The Sum is ${mSum}")
   
}

fun mCheckCondition(a:Int, b:Int): Int = if(a>b)
    { 
    println("A is Greater")
    a 
    } else {
    println("B is Greater")
    b // It will always return the last line
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

## Default Function Parameters

-  If the function is called without passing arguments then the default arguments are used as function parameters.

__Example__

```ruby
fun main() {

  mGetDetails(1, 2)
  
  mGetDetails(10, 20, 25) // TODO Where 25 will Overrides the Default Value 10

}

fun mGetDetails(mValueOne: Int, mValueTwo: Int, mValueThree: Int = 10) { // TODO Default Parameters in Parameters
  println("$mValueOne $mValueTwo $mValueThree")
}
```
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

## Named Parameters  

- Kotlin allows you to specify the names of arguments that you're passing to the function. 
- This makes the function calls more readable. 
- It also allows you to pass the value of a parameter selectively if other parameters have default values
- It's a pure Kotlin Functionality which is not present in Java.

__Example__

```ruby
fun main() {

  mGetMarkDetails(mMarksScored = 45, mName = "Gauthy") // TODO Named Parameters

}

fun mGetMarkDetails(mName: String, mMarksScored: Int, mPass: String = "Pass") {

  println("Name is $mName and Secured $mMarksScored. So the Result is $mPass")

}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

## Null Safety Operators

- It is mainly used to avoid the Null Pointer Exception so that the normal flow of Application can be Maintained.
- Types -> Nullable Types and Non-Nullable Types

__Nullable Types__

- Nullable types are declared by putting a ? behind the String.  

__Example__

```ruby
fun main() {

  var name: String? = "Android"
  name = null

  print(name)

}
```

__Non Nullable Types__

- Non nullable types are normal strings which are declared as String.

__Example__

```ruby
fun main() {

  var name: String = null // TODO Compile Time Error

}
```  

__Safe call (?.)__

- We can print the Value only if the Value is not null it will print or else it will returns the null.

__Example__

```ruby
fun main() {
  
  var mString: String? = null
  println(mString)

}
```  

__Safe Call with let ( ?.let )__

- It Executes the block only if the Value is not null.

__Example__

```ruby
fun main() {

  var mString: String = "valueOne"

  mString?.let {
    println(mString)
  }

}
```  

__Elvis Operator ( ?: )__

- We can print the Value only if the Value is not null or else set the default value.

__Example__

```ruby
fun main() {

  var mString: String = "valueOne"

  val mValidate = mString?.length ? : 0

  print(mValidate)

}
```  

__Non-null assertion Operator ( !! )__ 

- Once we are sure the value is not null we can use it or else it will throw a Null pointer exception.  

__Example__

```ruby
fun main() {

  var mString: String = "valueOne"

  print(mString!!.length)

}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

## Lateinit Keyword

- It can be Used when Values of the Variables which are initialized only in the Future.
- It is applicable only with mutable[ var ] and non-nullable data types.

__Need to Know,__

- If we try to access the lateinit variable without initializing the value then it will throw a UninitializedPropertyAccessException at the run time.  

__Example__

```ruby
fun main() {
  
  lateinit var mString: String // TODO using lateinit keyword to initialize the value in Future
  mString = "Hello World!!!"
  println(mString)

}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

## Lazy Initialization  

- It is mainly used to prevent unnecessary initialization of Objects.
- Variables will not be initialized unless we not use it in our Code.
- If we initialize once then we will get the value from cache memory by next time Which makes the thread safe.
- It is applicable only with immutable[ val ] and non-nullable data types. 

__Need to Know,__

- lazy can only be used for val properties, whereas lateinit can only be applied to var because it can't be compiled to a final field, thus no immutability can be guaranteed. 

__Example__

```ruby
fun main() {
    
    val mInt: Int by lazy {3} 
    
    println(mInt * 3) // TODO mInt will get initilaized only for the First Time
    println(mInt * 4) // TODO For the Second Time it will load from the Cache Memory
 
}
```  
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  

	
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

:arrow_up: [__Back to Top__](Basics.md#table-of-contents)
