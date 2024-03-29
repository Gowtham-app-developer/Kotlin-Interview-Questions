# Examples  

## var & val

__Example__

```ruby
fun main() {

  var mValueOne = "Two" // TODO - Mutable String 
  mValueOne = "One"
  println(mValueOne)

  val mValueTwo = "Two" // TODO - Immutable String
  // mValueTwo = "Two" // TODO - It will Get Compile Time Error
  println(mValueTwo)

  var mValueThree: String // TODO - Explicitly defined the String
  mValueThree = "Three"
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

        5,9 -> "x is 5 (or) 9" // TODO - Checking for multiple values using comma seperation
        in 10..19 -> "x is 10 (to) 19" // TODO - Checking for multiple values using dot
        !in 10..19 -> "x is 10 (to) 19"
        1 -> "x is 1"
        2 -> "x is 2"
        else -> {
            "x value is Gauthy"
            "x is an Gowtham"
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
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions#interoperability)

## Extension Function

__Example 1__

```ruby
fun main() {

    var mStudent = Student()

    println("Result: ${mStudent.mGetMarkDetails(45)}")

    println("Result: ${mStudent.mGetAdmissionDetails(2009)}")
}

fun Student.mGetAdmissionDetails(mValue: Int): Boolean { // TODO Extension Function
    return mValue < 2000
}

class Student {

    fun mGetMarkDetails(mValue: Int): Boolean {
        return mValue > 40
    }
}
```  

__Example 2__

```ruby
fun main() {

    val mString1: String = "Hello "
    val mString2: String = "World"
    val mString3: String = "Hey "

    println(mString3 + mString1 + mString2) // TODO With out creating the Extension Function the code will be like this

    println(mString3.add(mString1, mString2)) // TODO Calling the Extension Function

    val mValue1: Int = 10
    val mValue2: Int = 20

    val mGreaterValue = mValue2.greaterValue(mValue1) // TODO Calling the Extension Function

    println(mGreaterValue)
}

fun String.add(mValueOne: String, mValueTwo: String): String { // TODO Creating Extension Function
    return this + mValueOne + mValueTwo // TODO Where this keyword refers to the mString3
}

fun Int.greaterValue(mValueOne: Int): Int { // TODO Creating Extension Function
    if (this > mValueOne) return this else return mValueOne // TODO Where this keyword refers to the mValueTwo
}
```  
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions#extension-function)

## Infix Function

__Example__

```ruby
fun main() {

    val mValue1: Int = 10
    val mValue2: Int = 20

    val mGreaterValue = mValue2 greaterValue mValue1 // TODO mValue2.greaterValue(mValue1)

    println(mGreaterValue)
}

infix fun Int.greaterValue(mValueOne: Int): Int { // TODO Creating infix Function
    if (this > mValueOne) return this else return mValueOne
}
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions#infix-function)

## Tailrec [Recursive] Function

__Example__

```ruby
fun main(args: Array<String>) {

    println(getFibonacciNumber(1000, BigInteger("1"), BigInteger("0")))
}

private tailrec fun getFibonacciNumber(
    n: Int,
    a: BigInteger,
    b: BigInteger
): BigInteger { // By Using the tailrec keyword

    return if (n == 0) b else getFibonacciNumber(n - 1, a + b, a)
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
        println("The Sum is ${mName}")
    }
    
}
```
__Example using Secondary Constructor__

```ruby
fun main() {

    var mValueOne = Employee("Kholi")

    var mValueTwo = Employee("Raja", 16)
    mValueTwo.mName = "Gowtham"

    println("The Sum is ${mValueTwo.mName}")
}

class Employee(var mName: String) {

    var mVarName: String = "Ganesh"

    init {
        println("The Sum is ${mName}")
    }

    constructor(_mName: String, mAge: Int) : this(_mName) {
        println("The Sum is ${_mName} and ${mAge}")
    }
}
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#init-keyword)  

## Inheritance

__Example__

```ruby
fun main() {

    var dog = Dog()
    dog.bread = "labra"
    dog.bark()
    dog.eat()

    var cat = Cat()
    cat.age = 7
    cat.meow()
    cat.eat()

    var animal = Animal()
    animal.color = "Green"
    animal.eat()
}

open class Animal { // TODO Using open keyword it can be accessible to other classes

    var color: String = ""

    open fun eat() {
        println("Eat")
    }
}

class Dog : Animal() { // TODO This class is implicitly Public Final

    var bread: String = ""

    fun bark() {
        println("Bark")
    }

    override fun eat() {
        super.eat() // TODO Calling super class Method
        println("NonVeg")
    }
}

class Cat : Animal() {

    var age: Int = 0

    fun meow() {
        println("Meow")
    }

    override fun eat() {
        // TODO We are defining the Animal Name explicilty because the interface having the same
        // method name
        super<Animal>.eat()
        println("Veg")
    }
}
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#inheritance)  

## Visibility Modifiers

__Example__

```ruby
fun main() {

    var mPerson = Employee()

    var mStudent = Student()
    println(mStudent.mValueOne)
    // println(mStudent.mValueTwo) // TODO Not Applicable because private in Nature
    // println(mStudent.mValueThree) // TODO Not Applicable because protected in Nature
    println(mStudent.mValueFour)
}

open class Person {

    public var mValueOne: String = "Data_1"
    private var mValueTwo: String = "Data_2"
    protected var mValueThree: String = "Data_3"
    internal var mValueFour: String = "Data_4"
}

class Employee : Person() {

    init {
        println(mValueOne)
        // println(mValueTwo) // TODO Not Applicable because private in Nature
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

## Abstract Class

__Example__

```ruby 
fun main() {

    val mStudent = Student()
    mStudent.mStudy()
    mStudent.mEat()
    mStudent.mWork()
}

abstract class Person {

    abstract fun mWork() // TODO abstract properties are "open" by default  
    
    open fun mStudy() { // TODO open Method
        println("Kotlin")
    }  
    
    fun mEat() { // TODO default Method
        println("Dhosa")
    }
}

class Student : Person() { // TODO Subclass or Derived Class

    override fun mWork() { // TODO Method Must Override or it will throw compile time error
        println("Developer")
    }
}
```  
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#abstract-class)  

## Interface

__Example__

```ruby
fun main() {

    val mButton = MyButton()
    mButton.onTouch()
    mButton.onClick()
}

// TODO Interfaces are not a class and it consists of both abstract and normal methods.  

interface MyInterfaceListener {  

    var mInt: Int // TODO By default the properties present in an interface are abstract.

    fun onTouch() // TODO By default the methods present in an interface are abstract.

    fun onClick() { // TODO Normal Methods are public and Open not final
        println("Dhosa")
    }
}

interface MySecondInterfaceListener { 

    var mInt: Int // TODO By default the properties present in an interface are abstract.

    fun onTouch() // TODO By default the methods present in an interface are abstract.

    fun onClick() { // TODO Normal Methods are public and Open not final
        println("Two Dhosa")
    }
}

class MyButton : MyInterfaceListener, MySecondInterfaceListener { // TODO Subclass or Derived Class

    override var mInt: Int = 1

    override fun onTouch() { // TODO Method Must Override or it will throw compile time error
        println("Developer")
    }

    override fun onClick() {
        super<MyInterfaceListener>.onClick()
        super<MySecondInterfaceListener>.onClick()
        println("Idli")
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

    // TODO Comparing Two Object References but by using Data class it will compare only the Values

    if (user1 == user2) println("Equal") else println("Not equal")

    println(
        user1.toString()
    ) // TODO The Data class will give the default implementation of toString()

    // TODO Copy the data from the user1 to other user and also  we can change the values
    var newUser = user1.copy(id = 40)
    println(newUser)
}

data class User(var name: String, var id: Int)
```
:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#data-class)  

## Object Keyword

__Example 1__

```ruby
fun main() {

    println("${Student.mStandard()}")

    Student.mSound()
}

open class Animals {

    open fun mSound() {
        println("Woww")
    }
}

object Student : Animals() {

    var mId: Int = 1 // TODO Behaves like a Static Variable

    fun mStandard(): String { // TODO Behaves like a Static Method
        return "Gauthy is Studying 4th Standard C Section"
    }

    override fun mSound() { // TODO It Supports Inheritance
        super.mSound()
        println("Woww2")
    }
}
```  

:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#object-keyword)  

## Companion Object

__Example__

```ruby
fun main() {

    Students.mSound()
}

class Students {

    companion object {
        fun mSound() { // TODO Behaves like a Static
            println("Woww")
        }
    }
}
```  

:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#companion-object)  

## Enum

__Example 1__

```ruby
enum class CreditCardType {
    SILVER, // TODO Ordinal = 0, name = "SILVER"
    GOLD, // TODO Ordinal = 1, name = "GOLD"
    PLATINUM // TODO Ordinal = 2, name = "PLATINUM"
}

fun main() {

    // TODO Enum constants are objects of enum class type.
    val mCardType: CreditCardType = CreditCardType.GOLD

    // TODO Each enum object has two properties: ordinal and name
    println(CreditCardType.GOLD.ordinal)
    println(CreditCardType.GOLD) // TODO (OR) CreditCardType.GOLD.name

    // TODO Each enum object has two methods: values() and valueOf()
    val myConstants: Array<CreditCardType> = CreditCardType.values() // TODO It returns array of Objects
    myConstants.forEach { println(it) }

    // TODO Using in 'when' statement
    when (mCardType) {
        CreditCardType.SILVER -> println("Gauthy has silver card")
        CreditCardType.GOLD -> println("Gauthy has gold card")
        CreditCardType.PLATINUM -> println("Gauthy has platinum card")
    }
}
```

__Example 2 (Using Constructor)__

```ruby
enum class CreditCardType(
    val color: String,
    val maxLimit: Int = 1000
) { // TODO Setting Default Value in Second Parameter
    SILVER("Red", 500),
    GOLD("White"),
    PLATINUM("Green")
}

fun main() {

    // TODO Enum constants are objects of enum class type.
    println(CreditCardType.GOLD.color)
    println(CreditCardType.GOLD.maxLimit)
}
```
__Example 3 (Using Interface)__

```ruby
enum class CreditCardType(val color: String, val maxLimit: Int = 1000) : MCardCashBack {
    SILVER("Red", 500) {
        override fun getCashbackValue(): Int {
            return 1
        }
    },
    GOLD("White") {
        override fun getCashbackValue(): Int = 10
    },
    PLATINUM("Green") {
        override fun getCashbackValue(): Int = 100
    },
}

interface MCardCashBack {
    fun getCashbackValue(): Int
}

fun main() {

    println(CreditCardType.GOLD.getCashbackValue())
}
```

:arrow_left: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#companion-object)  

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
