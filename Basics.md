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

    println("The name of the person is ${personObj.name}")
    
    personObj.details("Jhon")
}

class Person {

    var name: String = ""
    
    fun details(mValue: String){
         println("The name of the person is " + mValue)
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

## Need to Know

- REPL -> Read-Eval-Print-Loop ( Tools -> Kotlin -> Kotlin REPL )
