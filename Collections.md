
## Collection & Array

- A collection usually contains a number of objects of the same type and these objects in the collection are called elements or items.
- Arrays are Mutable but have fixed size.
- Types -> Immutable Collections, Mutable Collections
- Immutable Collections -> Read Only Operations can not modify its elements.
- It consists of the Following Methods (i.e.) Immutable List – listOf() and listOf<T>(), Immutable Set – setOf(), Immutable Map – mapOf()
- Mutable Collections -> It supports both read and write functionalities.
- It consists of the Following Methods (i.e.) Mutable List – mutableListOf(), arrayListOf() and ArrayList, Mutable Set – mutableSetOf(), hashSetOf(), Mutable Map – mutableMapOf(), hashMapOf() and HashMap
- Arrays in Kotlin are mutable in nature but have Fixed Size.
- Arrays is a collection of Elements (i.e.) Int, Strings and So on.
    
__Example (Using Array)__
    
```ruby
fun main() {

  // TODO Elements: 1 1 1 1 1
  // TODO Index   : 0 1 2 3 4   

  var mArrayList = Array < Int > (5) { // TODO Mutable, Fixed Size
    1
  } // TODO inside the Lambda we have to define the initial value of all the Elements. 

  mArrayList[3] = 2

  println(mArrayList[3])

  for (mElements in mArrayList) {
    print(mElements)
  }

  for (mIndex in 0..mArrayList.size - 1) {
    println(mIndex) 
  }

}    
```  
    
__Example (Using listOf)__
    
```ruby
fun main() {

  var mList = listOf < String > ("Apple", "Cat", "Kotlin", "Dart") // TODO Immutable, Fixed Size, Read Only

  for (mElements in mList) { // TODO Using Individual Element (i.e) Objects
    print(mElements)
  }

  for (mIndex in 0..mList.size - 1) {  // TODO Using Index of the Element (i.e) Objects
    println(mList[mIndex]) // TODO also we can use mList.get(mIndex)
  }

}
``` 
    
__Example (Using mutableListOf, arrayListOf, ArrayList)__
    
```ruby
fun main() {
 
 var mList = mutableListOf<String>("Apple") // TODO Instead of mutableListOf, we can also use arrayListOf, ArrayList
 mList.add("Cat") // TODO Mutable, No Fixed Size, Can Add or Remove Elements
 mList.add("Ball")
 
 mList.remove("Cat")
 mList.add(1, "Kotlin")
 
 mList[1] = "Hello"
 
  for(mElements in mList){
        print(mElements)
    }
    
    for(mIndex in 0..mList.size-1){
        println(mList[mIndex])
    }    
	
}
```
    
:arrow_up: [__Back to Top__](Basics.md#table-of-contents)   
	
## Map

- The Map is actually a Data Structure which contains the Elements in the form of Key-Value Pair.
- It is Immutable (i.e.) We can Read Only & it has Fixed Size.		
	
__Example (Using mapOf)__  
	
```ruby	
fun main() {

  var mMap = mapOf < Int, String > (1 to "Apple", 3 to "Orange", 2 to "Mango", 5 to "Grapes") 

  for (mKey in mMap.keys) { 
    println("$mKey = ${mMap[mKey]}") // TODO Instead mMap[mKey] also we can use mMap.get(mKey)
  }

}	
```  
	
## HashMap
	
- It contains the Elements in the form of Key-Value Pair.
- A HashMap is unsynchronized and it permits null as a key. 
- HashMap is Mutable (i.e.) We Can Add or Remove Elements & No Fixed Size.
	
__Example (Using HashMap, mutableMapOf, hashMapOf)__  	

```ruby
fun main() {

  var mMap = HashMap < Int, String > () // TODO Instead of HashMap, We can also use hashMapOf().
  
  mMap.put(1, "Apple")
  mMap.put(3, "Pineapple") 
  mMap.put(2, "Grapes")
  mMap.put(5, "Orange")
  
  mMap.put(2, "Mango")
  
  mMap.replace(2, "Stawberry")

  for (mKey in mMap.keys) {
    println("$mKey = ${mMap[mKey]}") // TODO We can also use mMap.get(mKey)
  }

}	
```	

## LinkedHashMap
	
- Similar to a HashMap, A LinkedHashMap in Kotlin implements a key value pair, it in facts extends the HashMap class.
- The LinkedHashMap maintains insertion order for the keys. 
- This is useful, when you would like the elements to retain the order of insertion.
	
__Example (Using LinkedHashMap)__  	

```ruby
fun main() {

  var mMap = LinkedHashMap < Int, String > () // TODO Instead of LinkedHashMap, we can also use mutableMapOf().
  
  mMap.put(1, "Apple")
  mMap.put(3, "Pineapple") 
  mMap.put(2, "Grapes")
  mMap.put(5, "Orange")
  
  mMap.put(2, "Mango")
  
  mMap.replace(2, "Stawberry")

  for (mKey in mMap.keys) {
    println("$mKey = ${mMap[mKey]}") // TODO We can also use mMap.get(mKey)
  }

}	
```	
	
## TreeHashMap  
	
- A TreeMap in Kotlin implements a sorted key value pair.
- The TreeMap maintains sorted order for the keys. 
- This is useful, when you would like the elements to be organized in sorted order.
	
__Example__
	
```ruby
import java.util.TreeMap

fun main() {

  var mMap = TreeMap < Int, String > () 
  
  mMap.put(1, "Apple")
  mMap.put(3, "Pineapple") 
  mMap.put(2, "Grapes")
  mMap.put(5, "Orange")
  
  mMap.put(2, "Mango")
  
  mMap.replace(2, "Stawberry")

  for (mKey in mMap.keys) {
    println("$mKey = ${mMap[mKey]}") // TODO We can also use mMap.get(mKey)
  }

}
```
	
## Set

- Set interface is a generic unordered collection of elements and it does not contain duplicate elements.
- Two Types -> setOf() & mutableSetOf() 	
- setOf() is Immutable (i.e.) We can Read Only & it has Fixed Size.	
- mutableSetOf() prints the value in the form of Sequence.
- mutableSetOf() is Mutable (i.e.) We Can Add or Remove Elements & No Fixed Size.
	
__Example [Using setOf]__  
	
```ruby	
fun main() {

  var mList = setOf < String > ("Apple", "Pineapple", "Grapes", "Orange", "Grapes")

  for (mElements in mList) {
    println(mElements)
  }

}	
```  		
	
__Example [Using mutableSetOf]__  
	
```ruby	
fun main() {

  var mList = mutableSetOf < String > () 
  
  mList.add("Orange")
  mList.add("Pineapple")
  mList.add("Apple")
  mList.add("Grapes")
  mList.add("Grapes")
 

  mList.remove("Pineapple")

  mList.add("Mango")

  for (mElements in mList) { 
    println(mElements)
  }

}	
```	
	
## HashSet 

- HashSet implements the Set interface. 
- There can be no duplicates in a HashSet. 
- There is no guarantee for the order of the elements in a HashSet.
- HashSet is Mutable (i.e.) We Can Add or Remove Elements & No Fixed Size.
	
__Example [Using hashSetOf]__  
	
```ruby	
fun main() {

  var mList = hashSetOf < String > ("Apple", "Pineapple", "Grapes", "Orange", "Grapes") 

  mList.remove("Pineapple")

  mList.add("Mango")

  for (mElements in mList) { 
    println(mElements)
  }

}
```			

__Example [Using HashSet]__  
	
```ruby	
fun main() {

  var mList = HashSet < String > () 
  
  mList.add("Apple")
  mList.add("Grapes")
  mList.add("Pineapple")
  mList.add("Grapes")
  mList.add("Orange")

  mList.remove("Pineapple")

  mList.add("Mango")

  for (mElements in mList) { 
    println(mElements)
  }

}
```
	
## TreeSet
	
- TreeSet is a collection of type Set, that provides & maintains sorted order of elements. 
- It does not contain duplicate elements.
- TreeSet implements the SortedSet interface.	
- TreeSet is Mutable (i.e.) We Can Add or Remove Elements & No Fixed Size.
	
__Example (Using mutableSetOf)__  
	
```ruby	
import java.util.TreeSet

fun main() {

  var mList = TreeSet < String > () 
  
  mList.add("Orange")
  mList.add("Pineapple")
  mList.add("Apple")
  mList.add("Grapes")
  mList.add("Grapes")
 

  mList.remove("Pineapple")

  mList.add("Mango")

  for (mElements in mList) { 
    println(mElements)
  }

}
```
