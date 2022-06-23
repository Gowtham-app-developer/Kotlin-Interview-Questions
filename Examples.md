# Examples  

## var & val

__Example__

```ruby
fun main() {

    var mValueOne = "One" // Mutable String 
    mValueOne = "Two" 
    println(mValueOne)
    
    val mValueTwo = "One" // Immutable String
    // mValueTwo = "Two"
    println(mValueTwo)
    
    var mValueThree: String // Explicitly defined the String
    mValueThree = "One"
    println(mValueThree)
    
}
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions#var--val)  

## When as Expression  

__Example__

```ruby
fun main(args: Array<String>) {

    val x = 110

    val str: String  = when (x) {

        5,9 -> "x is 5 (or) 9" // Checking for multiple values using comma seperation
        in 10..19 -> "x is 10 (to) 19" // Checking for multiple values using dot
        !in 10..19 -> "x is 10 (to) 19"
        1 -> "x is 1"
        2 -> "x is 2"
        else -> {
            "x value is unknown"
            "x is an alien"
        }
    }

    println(str)
}
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions#when-as-expression)  

## Interoperability  

__Example using Java__

```ruby
public class JavaFile {

	public static void main(String[] args) {

		int sum = MyKotlinInteroperabilityKt.addNumbers(13, 4);
		System.out.println("Printing sum from Java file :" + sum);
	}

	public static int getArea(int l, int b) {
		return l * b;
	}
}
```  

__Example using Kotlin__

```ruby
fun main(args: Array<String>) {

    var area = MyJavaFile.getArea(10, 50)
    println("Printing area from Kotlin file: $area")
}

fun addNumbers(a: Int, b: Int): Int {
    return a + b
}
```

## Tailrec [Recursive] Function

__Example__

```ruby
 fun main(args: Array<String>) {

        println(getFibonacciNumber(1000, BigInteger("1"), BigInteger("0")))
    }

    private tailrec fun getFibonacciNumber(n: Int, a: BigInteger, b: BigInteger): BigInteger { // By Using the tailrec keyword

        return if (n == 0)
            b
        else
            getFibonacciNumber(n - 1, a + b, a)
    }
```  

:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions#tailrec-recursive-function)

## Init Keyword

__Example using Primary Constructor__

```ruby
fun main() {	
  
    var mValue = Employee ("Raja")
    mValue.mName = "Gowtham"
    
    println("The Sum is ${mValue.mName}")
    
}

class Employee(mName:String){
    
  var mName:String = "Gokul"
    
    init{
        print("The Sum is ${mName}")
    }
    
}
```
__Example using Secondary Constructor__

```ruby
fun main() {	
  
    var mValueOne = Employee ("Kholi")
    
    var mValueTwo = Employee ("Raja", 16)
    mValueTwo.mName = "Gowtham"
    
    println("The Sum is ${mValueTwo.mName}")
    
}

class Employee(var mName:String){
    
  var mVarName:String = "Ganesh"
    
    init{
        println("The Sum is ${mName}")
    }
    
    constructor(_mName:String, mAge:Int):this(_mName){
        println("The Sum is ${_mName} and ${mAge}")
    }
   
}
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#init-keyword)  

## Visibility Modifiers

__Example__

```ruby
fun main() {	
  
   var mPerson = Employee()
   
   var mStudent = Student()
   println(mStudent.mValueOne)
   // println(mStudent.mValueTwo)
   // println(mStudent.mValueThree)
   println(mStudent.mValueFour)
    
}

open class Person{
  
    public var mValueOne: String = "Data_1"
    private var mValueTwo: String = "Data_2"
    protected var mValueThree: String = "Data_3"
    internal var mValueFour: String = "Data_4"
   
}

class Employee : Person() {
    
    init{
        println(mValueOne)
        // println(mValueTwo)
        println(mValueThree)
        println(mValueFour)
    }
   
}

class Student {
    
    public var mValueOne: String = "StuData_1"
    private var mValueTwo: String = "StuData_2"
    protected var mValueThree: String = "StuData_3"
    internal var mValueFour: String = "StuData_4"
   
}
```  
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#visibility-modifiers)  

## Interface

__Example__

```ruby
fun main(args: Array<String>) {

    var mPerson = Person()
    mPerson.mSubmitButtonClick()
    mPerson.mToastButtonClick()
}

interface myButtonClick{

    fun mSubmitButtonClick()
    
    fun mToastButtonClick(){
        
    }
    
}

class Person : myButtonClick {
    
    override fun mSubmitButtonClick(){
        println("Button is Clicked")
    }
    
     override fun mToastButtonClick(){
        super<myButtonClick>.mToastButtonClick()
        println("Toast Button is Clicked")
    }
}
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#interface)  

## Data Class

__Example__

```ruby
fun main(args: Array<String>) {

    var user1 = User("Gowtham", 10)

    var user2 = User("Raja", 20)
    
    if (user1 == user2)
        println("Equal")
    else
        println("Not equal")
        
    println(user1.toString())

    var newUser = user1.copy(id = 40)
    println(newUser)
}

data class User(var name: String, var id: Int)
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#data-class)  

## Higher Order Functions

__Example 1__

```ruby
fun main() {	
   
var mName:String ="Hello" 
    
fun Student(a:String){ // Normal Function
    println("a")
}

var mNameOne: String = fun Student(a:String){ // Normal Function assigned to a Variable
    println("a")
}
    

var mNameOne: (String) -> Unit = { a:String -> println("a")} // Higher Order Function assigned to a Variable

{ a:String -> "Hello"} // Lambda Experssion

}
```  

__Example 2__

```ruby
fun main(args: Array<String>) {

    val program = Program()

    program.addTwoNumbers(2, 7)

    program.addTwoNumbers(2, 7, object : MyInterface {   // Using Interface

        override fun execute(sum: Int) {
            println(sum) // Body
        }
    })

    val test: String = "Hello World"

    val myLambda: (Int) -> Unit = { s: Int -> println(s)} // Lambda Expression [ Function ]
    program.addTwoNumbers(2, 7, myLambda)
}

class Program {

    fun addTwoNumbers(a: Int, b: Int, action: (Int) -> Unit) {  // High Level Function with Lambda as Parameter

        val sum = a + b
        action(sum)   // println(sum)
    }

    fun addTwoNumbers(a: Int, b: Int, action: MyInterface) { // Using Interface 
        val sum = a + b
        action.execute(sum)
    }

    fun addTwoNumbers(a: Int, b: Int) { // Simple way

        val sum =  a + b
        println(sum)
    }
}

interface MyInterface {
    fun execute(sum: Int)
}
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#higher-order-functions)  
