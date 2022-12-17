# Kotlin-Interview-Questions


## Table of Contents

| S.No | Content |
| --------	 | ------------ |
| 1 | [Kotlin](README.md#kotlin) |
| 2 | [Why Kotlin](README.md#why-kotlin) |
| 3 | [var & val](README.md#var--val) |
| 4 | [When as Expression](README.md#when-as-expression) |
| 5 | [Interoperability](README.md#interoperability) |
| 6 | [Extension Function](README.md#extension-function) |
| 7 | [Infix Function](README.md#infix-function) |
| 8 | [Tailrec [Recursive] Function](README.md#tailrec-recursive-function) |
| 9 | [Init Keyword](README.md#init-keyword) |
| 10 | [Inheritance](README.md#inheritance) |

## Kotlin

- It is a Statically Typed Programming Language (i.e.) Data type must be defined.
- It is Officially announced for Android Development.
- It is Powerful and Easy to Use.
- It Uses JVM to execute its byte code.

:arrow_up: [__Back to Top__](README.md#table-of-contents)

## Why Kotlin

- To Avoid NullPointer Exception (i.e.) It provides Null Safety.
- It Supports Immutability (i.e.) We can use val.
- It Supports Oops concepts.
- It Supports Functional Programming (i.e.) Can pass Function as parameter to another function or Function can return another function.
- Write only Less Code (i.e.) It Reduces a lot of Boilerplate Code.

:arrow_up: [__Back to Top__](README.md#table-of-contents)

## var & val

- Var is mutable (i.e.) Values of the variable can be changed later.
- Val is immutable (i.e.) Values of the variable cannot be changed later.

__Need to Know,__

- In Kotlin, We use Capital Letters for defining the Data Types and there is no primitive Data Type.
- Data Types in Kotlin all are objects so it must be initialized (i.e.) There is no default value for the Data Types.
- Try to use Float instead of Double, because it consumes Less memory size.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#var--val)

:arrow_up: [__Back to Top__](README.md#table-of-contents)  

## When as Expression

- In Kotlin, When replaces the switch case Statement which it can be used in two ways -> when as a statement and when as an expression 
- It doesn't require a break statement at the end of each case.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#when-as-expression)

:arrow_up: [__Back to Top__](README.md#table-of-contents)

## Interoperability

- We Can Call Java Functions from Kotlin and Kotlin Functions from Java using some annotations.
- We Can have both Java and Kotlin files in the same Application.
- __Example:__ Java doesn’t support default Functions but we can achieve using @JVMOverloads in Kotlin.

__Need to Know__  

- In Java, During Compile Time -> Compiler will Java Code will convert (i.e.) MainActivity.java in to Byte Code (i.e.) MainActivity.class
- In Koltin,  During Compile Time -> Compiler will Kotlin Code will convert (i.e.) MainActivity.java in to Byte Code (i.e.) MainActivityKt.class  

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#interoperability)

:arrow_up: [__Back to Top__](README.md#table-of-contents)  

## Extension Function

- We Can add Functions to the class without declaring it.
- It is Similar to that of Static(i.e) Kotlin compiler converts into static functions Internally.
- They become part of our Own class(Model) and Predefined Class(String, Int).
- It Reduces the code and is easy to Understand.  

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#extension-function)

:arrow_up: [__Back to Top__](README.md#table-of-contents)  

## Infix Function  

- Infix Notation is most commonly used while doing arithmetical and logical Operations.
- It can be a Member Function or Extension Function.
- All Infix Functions are Extension Function but all Extension Function are not infix Function.
- Can have only one parameter and infix keyword as prefix.
- It increases the readability of the Code.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#infix-function)

:arrow_up: [__Back to Top__](README.md#table-of-contents) 

## Tailrec [Recursive] Function

- It is mainly used to prevent Stack Overflow Exception due to the limit of Stack Memory.
- Uses Recursion in a more Optimized way. [ Recursion  means calling your own function within the function ]
- We can print countless numbers without exception.
- Prefix of tailrec keyword is used.
- __Example:__ Fibonacci type of Applications.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#tailrec-recursive-function)

:arrow_up: [__Back to Top__](README.md#table-of-contents)

## Init Keyword

- In Kotlin, the primary constructor cannot contain any code.
- init blocks allows adding code to the primary constructor.
- The init block will execute immediately after the primary constructor.

__Need to Know__

- Unlike the Primary Constructor, the Secondary constructor has its own body and the primary constructor call is expected.
- We can’t declare the properties (i.e.) Val or Var in the Secondary Constructor.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#init-keyword)  

:arrow_up: [__Back to Top__](README.md#table-of-contents)  

## Inheritance

- It is the Process from which one object acquires all the properties and methods from its Parent Class.
- In Kotlin, By Default the classes are public and final which we could not inherit so we have to declare the class using an Open keyword.
- The Open keyword  allows other classes to inherit from this class.
- It provides Code Reusability and Method Overriding.
- Types - Single Inheritance, Multilevel Inheritance and Hierarchical Inheritance.
- __Note:__ Any Class is the base class (i.e.) Super class of all the classes present at the Top which it contains functions such as equals(), hashcode() and toString()

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#inheritance)

:arrow_up: [__Back to Top__](README.md#table-of-contents)  

## Visibility Modifiers

- It provides access control for classes, Functions etc.
- By using the Following keywords (i.e.) Public, Protected, internal and Private.
- By Default all the Classes and Functions are public in nature.
- __Public:__  We can access it anywhere (inside and even outside) the Class.
- __Private:__  We can access it only inside the Class.
- __Internal:__  We can access it only inside our module.
- __Protected:__  The Modifier Protected is not applicable for top level Function and Classes (i.e) It can be accessible only within a class or Subclass not     outside the Class.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#visibility-modifiers)

:arrow_up: [__Back to Top__](README.md#table-of-contents)  

## Abstract Class

- Abstract Classes are partially defined classes which are declared using abstract keywords.
- It can have both abstract (no body) and non-abstract methods (method with the body).
- If a class contains partial implementation then we should declare a class as abstract and it cannot be instantiated.
- If we define any properties or methods in abstract class then we must override that properties or methods in the sub class.
- In Kotlin, By default all the abstract Properties are "open" in nature.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#abstract-class)

:arrow_up: [__Back to Top__](README.md#table-of-contents) 

## Interface

- Interfaces are considered to be fully Abstract class but they are not a class which is declared using the keyword Interface.
- By default the properties and methods present in an interface are abstract.
- It consists of both abstract and normal methods.
- Normal methods are public and open by default not final.
- The variables are only in abstract Nature (i.e.) we cannot initialize any variables inside the interface.
- Similar to abstract class we cannot create an instance in Interface. 
- It is used to achieve abstraction and multiple inheritance.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#interface)

:arrow_up: [__Back to Top__](README.md#table-of-contents) 

## Data Class  

- Data Class internally contains functions such as equals(), hashCode(), toString() and copy() method too.
- The main purpose of the Data Class is to deal with the data, not with the Objects.
- In Data class the primary constructor should contain only with a property variable (i.e) [ val or var ]

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#data-class)

:arrow_up: [__Back to Top__](README.md#table-of-contents) 

## Object Keyword

- In Kotlin we cannot declare using Static Variables and Methods.
- By Using the Object keyword it creates a Singleton Object while it runs (i.e) it internally creates a class and an object/instance.
- By declaring Properties,Methods and Initializers present inside the Object keyword will act like a Static.
- We don’t need to create an instance Manually.
- It Cannot have constructors.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#object-keyword)

:arrow_up: [__Back to Top__](README.md#table-of-contents) 


## Higher Order Function

- The Function passed as parameter to another function or a Function can return another function or It can do both.
- It also simply accepts the lambda expression as a parameter to higher Order Functions or it can also return the lambda Function.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#higher-order-function)

:arrow_up: [__Back to Top__](README.md#table-of-contents) 

## Lambda Expression

- Lambdas expression and Anonymous function both are function literals meaning these functions are not declared but passed immediately as an expression. 
- In Simple, it is just a function with no names.

__Example:__ 

- Val myLambdaFunction: (Int, Int) -> Int = {x,y -> x+y} 
- Where, myLambdaFunction is the Variable Name
- Where, (Int, Int) -> Int is the Parameters and Return type of the method body.
- Where, x,y are parameters and x+y are method body
 
:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#lambda-expression)

:arrow_up: [__Back to Top__](README.md#table-of-contents) 

## Enum 

- Enum (Enumeration)  is a data type that contains a fixed set of constants which is declared using the keyword enum. 
- When we require a predefined set of values which represents some kind of data, we use enum. 
- In Java enum constants are implicitly static and final.

:arrow_right:  [__Click For Example__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/blob/main/Examples.md#enum)

:arrow_up: [__Back to Top__](README.md#table-of-contents) 

## View Model Factory

- If we need to pass some input data to the constructor of the viewModel, we need to create a factory class for viewModel.
- __Reason:__ We cannot directly create the object of the ViewModel as it would not be aware of the lifecyclerOwner.

__Example:__ 

```ruby
class MyViewModelFactory constructor(private val repository: DataRepository): ViewModelProvider.Factory {

     override fun <T : ViewModel> create(modelClass: Class<T>): T {
        return if (modelClass.isAssignableFrom(MyViewModel::class.java!!)) {
            MyViewModel(this.repository) as T
        } else {
            throw IllegalArgumentException("ViewModel Not Found")
        }
    }
}
```
```ruby
ViewModelProviders.of(this, MyViewModelFactory(repository)).get(MyViewModel::class.java)
```


# Bonus Questions

## How Koltin Works

- Koltin uses JVM to execute its byte code.
- The Koltin compiler internally creates a class file which is loaded into memory during the execution of Runtime
- __Example:__ If we MainActivity.kt -> it will converts in to MainActivitykt.class during the execution of Runtime

:arrow_up: [__Back to Top__](README.md#kotlin)

## Null safety in Kotlin

- Kotlin's type system is aimed at eliminating the danger of null references from code.
- Types -> Nullable Types and Non-Nullable Types

__Nullable Types__

- Nullable types are declared by putting a ? behind the String.

```ruby
var name: String? = "Android"  
name = null
```

__Non Nullable Types__

- Non nullable types are normal strings which are declared as String.

```ruby
val name: String = null // compile error  
```

__Null checks(!!)__

- The null check operator !! is used to inform the compiler that the property or variable is null or not. 
- If it is null then it will throw some NullPointerException.

```ruby
studentA!!.giveGoodies() //works fine if studentA is not null
```

__Safe call (?.)__

- In the below example, If any of the value is null i.e. if either of studentA, courseName, instructor is null then the whole expression will return null.

```ruby
studentA?.courseName?.instructor?.name 
```

__Safe call (?.) vs Null checks(!!)__

- The basic difference between the Safe call and Null check is that we use Null checks (!!) only when we are confident that the property can’t have a null value. 
- If we are not sure that the value of the property is null or not then we prefer to use Safe calls(?.).

__Elvis Operator (?:)__

- Elvis operator (?:) is used to return the not null value even the conditional expression is null. 
- It is also used to check the null safety of values.

```ruby
var name: String? = null  
var company: String? = "May be declare nullable string"  
var nameLength:  Int = name ?.length ?: -1  
var companyLength:  Int = company ?.length ?:  -1  
```

## const vs val

- In kotlin, const and val both represents the immutability and read only values and act as final keyword in java.
- val keyword must be used to declare for run time values and const keyword must be used to declare compile time values.
- const must be used only with primitive data types not for function and constructors.

```ruby
const val fun1 = anyFunctionOrConstructor() // it is not fine
val fun2 = anyFunctionOrConstructor() // it is perfectly fine      
const val a = "My String" // it is perfectly fine
```
