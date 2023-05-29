### 1. Introduction

Object-oriented programming, also known as OOP is a set of programming concepts and style that organizes code around objects. 

However, while OOP may be a programming style, it is essential to know the concepts of OOP, as many programming languages that support it such as Java, Python, JavaScript, the C family (C, C#, C++) and many more are designed with strong support for OOP. As such, the concepts of object-oriented programming form the foundation of these languages.

With that being said, there are 4 main concepts in object-oriented programming:
   1. Abstraction
   2. Polymorphism
   3. Encapsulation
   4. Inheritance

### 2. Abstraction

Abstraction is the concept of object-oriented programming that focuses on only displaying essential attributes and hiding unnecessary information. The main purpose of abstraction is to hide the unnecessary details from users.  
  
For example, when creating a **banking application**, you can abstract a few details from a larger list of data. 

For each customer, you are given the following information as the dataset:
   1. Full name
   2. Tax information
   3. Address
   4. Contact number
   5. Favourite food
   6. Favourite movie genre

Instead of using all the data you received in the dataset, you can abstract it down to just **full name**, **tax information**, **address**, and **contact number** of each customer, and use that as the dataset for the banking application. 

By removing unnecessary data, you allow better data management and also improved performance for the application as the application may not need to read as big of a file as before. 

The same abstracted data can also be used to serve other purposes, such as being given to hospitals, employee or government databases for their own records.

### 3. Polymorphism

Polymorphism is the concept whereby a single object is able to take on multiple forms.

When creating a class of similar types such as bicycles, instead of having separate classes with separate properties for each type of bike, their similar properties should be grouped into a single class such as the `Bicycle` class with each type of bike (subclass) inherit the `Bicycle` class (superclass).

An **inefficient** example is done in Java below:
```java
class MountainBike extends Bicycle {
	private String color;
    private int maxSpeed, maxGear;
}

class HybridBike extends Bicycle {
	private String color;
    private int maxSpeed, maxGear;
}

class RoadBike extends Bicycle {
	private String color;
    private int maxSpeed, maxGear;
}
```


A **more efficient** example is done in Java below:
```java
/*
 * There is a chance that the example code may not be valid Java, and as such the code   * should only be treated as an example of Polymorphism.
 */

class Bicycle {
    private String color = "red";
    private int maxSpeed, maxGear;
}

class MountainBike extends Bicycle {
	// Gets the `color`, `maxSpeed`, and `maxGear` objects without having to define it again.
}

class HybridBike extends Bicycle {
	// Gets the `color`, `maxSpeed`, and `maxGear` objects without having to define it again.
}

class RoadBike extends Bicycle {
	// Gets the `color`, `maxSpeed`, and `maxGear` objects without having to define it again.
}
```

Within Java, the `extends` keyword is a way to inherit classes, which also allows the subclasses to inherit the `color`, `maxSpeed` and `maxGear` variables without having to declare it again.

The **superclass** refers to the class being inherited, while the **subclass** refers to the class that is inheriting the superclass.

It is beneficial to know that although the variables are inherited across the 3 classes, it **does not mean** that the value of the variables are shared. If the variables are declared in the `Bicycle` class, the other variables in the subclasses will also have the same value as the `Bicycle` class. 

In the example, `color` was declared in the `Bicycle` class with the String `red`.  As such, the other classes also have `color` declared as `red`. However, changing the value of `color` in one of the subclasses will not affect the other classes. Similarly, `maxGear` and `maxSpeed` is not declared in the superclass (`Bicycle`), and as such the other classes also have `0`* for their `maxGear` and `maxSpeed`.

*\* Note: The classes have `0` as the value and not `null` as the data type `int` defined in the example is a primitive type. As such, it cannot be 0.*

As inheriting variables from the `Bicycle` class avoids the need for subclasses to declare the same few variables, this not only makes the code **look cleaner** but also allows the compiler to be more efficient.



### 3. Encapsulation

Encapsulation refers to restricting **direct access** to variables or methods. This prevents other classes from accessing these variables or methods.

Within Java, this is done using visibility modifiers in the form of the keywords `public`, `private` and `protected`, while Python uses naming conventions in the form of adding `_` (underscores) to the method or variable, which suggests that the method or variable is an internal component and should not be directly accessed from outside the class/module. 

However, the difference between Java and Python is that once visibility modifiers are set in Java, they are strictly enforced and other classes will not be able to access the specific variable/method if its set to `private`. As for Python, it is still possible to access the variables or methods as Python does not enforce strict visibility control.

For example,
```java
public class Person {
	private String creditCardNumber;
	private String name, gender;
	private int age;

	public int getAge() {
		return age;
	}

	public String getName() {
		return name;
	}

	public String getGender() {
		return gender;
	}

	// Note the `private` is used instead of public
	private String getCreditCardNumber() {
		return creditCardNumber;
	}
	
	private void setCreditCardNumber(int creditCardNumber) {
		this.creditCardNumber = creditCardNumber
	}
}
```

Within Java, each of the visibility modifiers modify the member as such:
   1. `public` - Member is visible to all classes, interfaces and enums, including classes outside of its own package.
   2. `private` - Member is only visible to the current class it is declared in.
   3. `protected` - Member is only visible to other members within the current package, as well as subclasses of the class it is declared in.

In the example, all the variables are set to `private` to prevent direct access to the variables by other classes. Instead of directly accessing the variables, getter and setter methods can be created for the variables which allow better access control to the variables.  

The getters for `name`, `age` and `gender` is set to public, allowing anyone to get the value. However, just like how you wouldn't give out credit card data in real life, the `getCreditCardNumber()` method is set to private, preventing other classes from directly accessing the data. Similarly, the `setCreditCardNumber()` method is also set to `private` to prevent other classes from directly modifying the data. Hence, the concept of encapsulation allows you to expose only specific members of a class to the public, while hiding certain members that you do not want available.


### 4. Inheritance

Inheritance is the concept whereby a class takes on the properties/methods of another class, with the reason being they share similar attributes and/or methods. This concept is displayed in polymorphism.


### 5. Conclusion

All in all, object-oriented programming is supported in many different languages, with most of them being popular ones. As such, it is important to understand these details so that your code is efficient in performing its work.