# Kotlin-Interview-Questions

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
:arrow_up: [__Back to Defintion__](main#init-keyword)

