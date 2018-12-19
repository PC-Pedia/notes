# Swift

## Basics

```swift
// Casting
var i:Int?=Int("2")
var i =Int("2")
var s:String? = String(2.3)
var s = String(22)
var car1 = truck1 as Car

// String
let strformat= "hello \(name\),\(age\)"
let multiLineString = """ xxx
xxx """

// loop
for index in 1..10 {}

// do-while
repeat{} while true

// Array
var ar:Double = [1.1,2.3]
var ar:Any = [1.1,2.3, "Any", true]
var names = [String]()
names.append("Ali")
name.remove("Ali")
name.remove(at:1)
var names2 = Array<String>()

// Sets
var names = Sets<String>()
names.insert("Ali")
names.insert("Ali")

// Dictionary
var dic:[Int:String]= [12:"Ali",22:""]
var dic= [12:"Ali",22:""]
var dic= [Int:String]()
dic[22]="Ali"  // adding
for (key, val) in dic{} // loop

// func
func sum(n1: Double, n2:Double) -> Double { return 0}

// class
class Car{
	var type:String?
	var price:Double?
	init(type:String){
		self.type=type
	}
	func getType()->String{
		return "A"
	}
}
var car1 = Car(type:"X")
car1.type="S"

// inheritance
class Truck:Car{
	override func getType()->String{
		return super.getType() + "Z" //AZ
	}
	override init(){ super.init("AZ") }
	private func foo(){}
}

// Interface - Protocol
protocol ILayer{
	func x(z:Int) - Int
}

// Extension
extension Car{
	func getPrice()->Int{
		return prise
	}
}
extension Double { func foo() {print(self)} }

// Enum
enum Direction { 
	case EAST
	case WEST
}
```