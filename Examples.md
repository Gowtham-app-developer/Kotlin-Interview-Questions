# Examples  

## Tailrec [Recursive] Function

__Example__

```ruby
 fun main(args: Array<String>) {

        println(getFibonacciNumber(1000, BigInteger("1"), BigInteger("0")))
    }

    private tailrec fun getFibonacciNumber(n: Int, a: BigInteger, b: BigInteger): BigInteger {

        return if (n == 0)
            b
        else
            getFibonacciNumber(n - 1, a + b, a)
    }
```  

:arrow_up: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions#tailrec-recursive-function)

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
:arrow_up: [__Back to Defintion__](https://github.com/Gowtham-app-developer/Kotlin-Interview-Questions/tree/main#init-keyword)

