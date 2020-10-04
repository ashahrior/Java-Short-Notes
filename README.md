


> Written with [StackEdit](https://stackedit.io/).
>

## Table of Contents
**[Introduction](#Introduction)**<br>
**[Syntax](#Syntax)**<br>
**[Data types, Operators and Expressions](#data-type-operator-expression)**<br>

## Intrdocution
* Any java code is written for a particular **Java Virtual Machine**. 
* The JVM **compiles** the code into intermediate code called **Bytecode**. Only JVM can understand the bytecode. 
* JVM **interprets** the bytecode into machine code during runtime. For this interpretation JVM uses **Just In Time (JIT)** compiler.
* Java is both compiled and interpreted language.
* **Bytecode** - a set of instructions only understandable by JVM.
* Java code is not written for any particular machine but for particular JVMs. Different operating system runs different JVM. But all JVM can run the same java code.
* **Just In Time (JIT)** compiler processes the bytecode produced by the compiler. It is also called **Dynamic Translator** as it processes bytecode during runtime.
* **JVM** is inside of **JRE**. **JRE** is inside of **JDK**.
* Java platform has 4 subsets -
	* Java Standard Edition - JSE
	* Java Enterprise Edition - JEE
	* Java Micro Edition - JME
	* JavaFX
* **Class loader** - A special class as a part of java runtime system. It loads necessary java compiled classes during runtime.

## Syntax
* A program must contain - **function** and **data**
* Package name always written in all lowercase letters.
* A java **method** has six parts-
	* Modifier
	* Return type
	* Method name
	* List of parameters
	* List of exceptions
	* Method body
Example:
		```java
		public String concat(String val1, String val2) throws IllegalArgumentException
		{
			if (val1==null) {
				throw new IllegalArgumentException('val1 is null");
			}
			if (val2==null) {
				throw new IllegalArgumentException('val1 is null");
			}
			return val1+val2;
		}
		```
* Java object creation consists of the following steps-
	* Declaration
	* Instantiation
	* Initialization
	Example: Here, 
	&nbsp;&nbsp;&nbsp;&nbsp; Bicycle bike - Declaration
	&nbsp;&nbsp;&nbsp;&nbsp; new - Instantiation
	&nbsp;&nbsp;&nbsp;&nbsp; Bicycle() - Initialization
	```java
	Bicycle bike = new Bicycle();
	```	
* Class constructor has no return type.
* If class constructor is not written explicitly then java compiler creates it implicitly before compilation. It is called **Default constructor**.
* If a class contains several constructors then they are differentiated on the basis of their respective arguments.
* **getter** method also called **accessor**.
* **setter** method also called **mutator**.
* Java method 2 types - 
	* Static method
		* It can't access non-static fields
		* It can't access object states
		* Doesn't require any object instantiation for access
		* Example: 
		```java 
		Integer.parseInt("26");
	* Non-static method
* Class import can be done in 2 ways-
	* Specific importing - Fully Qualified Name
	* Wildcard importing - using '*' sign

## Data type, Operator and Expression
* Four types of variables in java-
	* Instance variables (Non-static field)
	* Class variable (Static field)
	* Local variable - declared inside of the method body or any code-block
	* Parameters variable
	Example:
	```java
	class Example {
		int a;	\\ instance-variable
		static int b;	\\ class-variable
		void method(int c)	\\ 'c' is parameters variable
		{
			int d;	\\ local variable
		}
	```
* Java has two data types-
	* Primitive types - boolean, byte, short, char, int, long, float, double
	* Reference types - Every primitive type has its own reference type. These are called **Wrapper class** of primitive types. Examples: Boolean, Byte, Short, Char, Integer, Long, Float, Double
* Primitive types and wrapper class objects can be used interchangeably. This is called **Automatic Conversion**.
* Primitive type -> Reference type => Autoboxing
* Reference type -> Primitive type => Unboxing
* char default value is '\u000'
* Initializing without instantiation is called literal. Example: int x = 5; here 5 is a value and a literal.
* Smaller data types -> Larger data types => **Type conversion / Widening Primitive Conversion**
* In Java there are 19 types of **Type Conversions**.
* Larger data types -> Smaller data types => Type casting / Narrowing Primitive Conversion
* In Java there are 22 types of **Type Casting**.
* In Java, array is a special type of object. Even though it has no class, it is created dynamically during runtime. Like any other class or object in Java, array also inherits **java.lang.object** class.
* Accessing array elements using index is called **Array Access Expression**.
* An array can be declared even with an **Interface** or **Abstract Class**. In this case, its elements are the objects of that interface's **implemented class** or the objects of that abstract class's **concrete class**. Array can store **null** value as well.
* Array has a public final field called **length** that keeps record of the number of elements in array.
