## Adding Comment Line

```ruby
/**
 * This is one type of comment Line
 */

// This is the another type of comment line
```

## Calling an Variable from Another Class 

```ruby
fun main(args: Array<String>) {

    var personObj = Person()
    personObj.name = "Steve"

    print("The name of the person is ${personObj.name}")
}

class Person {

    var name: String = ""
}
```
