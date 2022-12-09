# Kotlin-Basics

## Table of Contents

| S.No | Content |
| --------	 | ------------ |
| 1 | [Adding Comment Line](Basics.md#adding-comment-line) |  
| 2 | [Declaring Variables and Methods](Basics.md#declaring-variables-and-methods) |  
| 3 | [String Interpolation](Basics.md#string-interpolation) |  
| 4 | [Calling Variables & Functions](Basics.md#calling-variables--functions-from-another-class) |
| 5| [By Using Primary Constrcutor](Basics.md#by-using-primary-constrcutor) |
| 6 | [Ranges](Basics.md#ranges) |
| 7 | [If as Expression](Basics.md#if-as-expression) |
| 8 | [For Loop](Basics.md#for-loop) |
| 9 | [While Loop](Basics.md#while-loop) |
| 11 | [do While Loop](Basics.md#do-while-loop) |
| 12 | [Break Statement](Basics.md#break-statement) |
| 13 | [Continue Statement](Basics.md#continue-statement) |
| 14 | [Function with Return Type](Basics.md#function-with-return-type) |
| 15 | [Function as Expression](Basics.md#function-as-expression) |
| 16 | [Need to Know](Basics.md#need-to-know) |

## Adding Comment Line

```ruby
/**
 * TODO - This is one type of comment Line
 */

// TODO - This is the another type of comment line
```
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)  


## Declaring Variables and Methods  

```ruby
fun main(args: Array<String>) {

    var mString: String // TODO Declaring Mutable String Explicitly
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
fun main(args: Array<String>) {

    for (i in 1..20) { // TODO - By using For Loop we will Initialize, check the condition, then print the Statement and finally we Increment.

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
fun main(args: Array<String>) {

    var i = 0 // TODO - In while Loop we will Initialize, check the condition, then print the Statement and finally we Increment.
    
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
fun main(args: Array<String>) {

    var i = 0

    do {
        if (i % 2 == 0) { // In do while Loop we will Initialize, print the Statement, then we Increment and finally we will do the condition check.
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

## Break Statement 

__Example_1__

```ruby
fun main(args: Array<String>) {

    for (i in 1..20) { 
            
            println(i)
            
           if(i==5){
              break // When the value becomes 5 then it won't stop further.
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
              break@mLoop // We used Labeled For Loop to reflect the changes in Outer For Loop
            println("$i $j")
         }
    }
 
}
```
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)

## Continue Statement 

```ruby
fun main() {	
   
mLoop@ for(i in 1..9){
         for(j in 1..9){
              if(i==2 && j==2)
              continue@mLoop // When the value become i == 2 and j == 2 it omits the Value and print further.
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
