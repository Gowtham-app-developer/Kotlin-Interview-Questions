# Kotlin-Basics

## Table of Contents

| S.No | Content |
| --------	 | ------------ |
| 1 | [Adding Comment Line](Basics.md#adding-comment-line) |
| 2 | [Calling Variables & Functions](Basics.md#calling-variables-functions-from-another-class-and-string-interpolation) |
| 3 | [var & val](README.md#var--val) |
| 4 | [When as Expression](README.md#when-as-expression) |
| 5 | [Interoperability](README.md#interoperability) |
| 6 | [Tailrec [Recursive] Function](README.md#tailrec-recursive-function) |
| 7 | [Init Keyword](README.md#init-keyword) |


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

## For Loop 

```ruby  
fun main(args: Array<String>) {

    for (i in 1..20) { // In For Loop we will Initialize, check the condition, then print the Statement and finally we Increment.

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

## While Loop 

```ruby
fun main(args: Array<String>) {

    var i = 0 // In while Loop we will Initialize, check the condition, then print the Statement and finally we Increment.
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
## Function with Return Type

```ruby
fun main() {	

   println("Sum is ${mAdd(2,3)}")
 
}

fun mAdd(a:Int, b:Int): Int {
    return a+b
}
```  

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
