# OOP questions

## Software design

### Error handling

#### What does 'fail fast' mean in terms of exception handling? Why is it a good practice?

in a case of failure the whole system will fail.

## Computer Science

### Data structures

#### How to find the middle element of singly linked list in O(n)?

create a pointer at the head of the list, and iterate over the list, until the end to find the length, then point at the end again. Get the linked element length/2 times.

#### Given an array of integers going from 1 to 100 (both inclusive) there is a duplicated entry. How to find it?

if the array is not sorted, sort it.
iterate over the array, and check if the current element is bigger than the previous one, if not, there is the duplicate.

#### What is a linked list? How to find if a linked list has a loop?

a linked list has an element called the head, and a method with which you can reach to another element.
if you declare the head element to an outer variable and iterate through the list, you can check if the current element is the same as the one declared. If the list comes to an end, it doesnt have a loop.

#### What is the Big O time complexity of the common operations in an ArrayList, LinkedList, HashMap? And of a bubble sort, quicksort, finding items in a Binary Search tree?
                Insert on index         Search by value         get by index        remove by value
ArrayList           O(N)                        O(N)                 O(1)                   O(N)
LinkedList          O(N)                        O(N)                 O(N)                   O(N)
HashMap             O(1)                        O(1)                 O(1)                   O(1)
bubble sort         O(n^2)
quicksort           O(nLogn)
binary search tree   O(n)

#### How does HashMap work?

A Hashmap is used for storing key-value pairs. We can get a List by parameterizing by key. We find this in exponentioaly short time, because we use some hash function to store the key initially. Then we check if the list containts the key we want to get, and that is has a value in it. If so, we return the element.

#### Why is it important for keys in a map to have an immutable type? (Consider String for example.)

If keys in the map were mutable, then after mutating them, their hashcode method might return a different integer than before. Since map uses the hashcode of the key for looking up a given entry, it would not find the entry anymore, beacuse its hashcode value now differs.

### Database

#### How can you connect your application to a database server? What are the possible ways?

You could use REST, and await response. Behind the backend we can create a connection to the server, get data by executing an sql command, get(or not) a return value, and close the connection.

#### What do you know about database normalization?

----------------------------------------------------

### Other

#### What is a garbage collector, in a nutshell?

it checks in once in a while throguh the running program if a variable has allocated memory which won't be used after. If such variable exists, it "collects the garbage" by resolving the variable.

## Programming paradigms

### Procedural

#### What is casting? What is the difference between up vs downcasting?
Downcasting:
Animal animal = new Dog();
Dog castedDog = (Dog) animal;

Up:
Animal animal = (Animal) animal

casting is when you force an object to be of another reference type.

#### Which order should we catch the exceptions? Why?

 when catching exceptions you want to always catch the most specific first and then the most generic (as RuntimeException or Exception).
 So we and the program know what went wrong exactly.

### Object-oriented

#### What is a class?

a class is a template for objects that share similar behaviours/properties

#### What is an object?

an object is an instance of a class, through which we can call methods and can handle data on an instance basis.

#### What is a constructor?

constructor of a class is a method which runs on instantiation. It is the first method to run.

#### Do we require parameter for constructors?

We can require parameters, but it is not compulsory

#### What is an interface?

It is an uninstantiable class that has method signatures in it, which must be implemented by the class that implements it.

#### What are access modifiers?

public, protected, private -these are keywords that regulates which classes see the methods, variables.

#### What is data hiding?

Data hiding ensures exclusive data access to class members and protects object integrity by preventing unintended or intended changes

#### Can a static method use non-static members?

No, it wouldn't make sense because a static method runs the same no matter of outside variables value

#### What is the difference between hiding a static method and overriding an instance method?

When you override a method, you still get the benefits of run-time polymorphism, and when you hide, you don't.
You can make a static method in a subclass, but that won't ensur polymorphism behaviour

#### Define the following terms: Instantiation, Attribute, Method

instantiation is when we create an instance with the new keyword. 
Attribute is a property of the created instance.
Method is an algorithm which you can call/invoke.

#### Could we access a static variable (or method) from a non-static method? Why?

yes, the goal is to run the same in each case.

#### Could we access a non-static variable (or method) from a static method? Why?

No, it wouldn't make sense because a static method runs the same no matter of outside variables value

#### How many instances you have of a static variable of a given class?

one

#### Why is it not a good practice to write a lot of static methods?

It is bad for Object Oriented design. The point of objects are that they are self-contained, they store data on an instance level. If you use a lot of static methods, you don't use behaviours that make it easier for build a system built on objects.

#### What are the features of static attributes and static methods of a class? What are the benefits, when to use them?

They are stored on a class level. They can be called even without instantiation through the class reference. 
They run the same each time
Use them when:
You need to use some data as constant. 
You need to share some data between instances and this data can be changed.
You need to separate extremely reusable code
You need to create a functionality that is tightly coupled with the implementation but it isn't linked with any instance (ENUMS)


#### What is the ‘this’ reference?

This references the current object we are in.


#### What are base class, subclass and superclass?

base class is a class from which other classes are derived.
sub class is the cass that derives from a class.
super class is the class from which the previous class derives directly.

#### Draw an object oriented family (as entities, with relations) on the whiteboard.

---------------------------

#### Difference between overloading and overriding?

Overloading is making multiple signatures from the method with the same name, overriding is 

#### What are the Object Oriented Principles? Explain the concepts with realistic examples!

Abstraction
Using abstract class/Interface we express the intent of the class rather than the actual implementation
Inheritance
expresses is-a has-a relationships. Dog is-a Animal.
Polymorphism A class has many forms, we can write a code that works on the superclass, and it will work with any subclass type as well. Also we can reference an obect by an interface it implements
Encapsulation
Restricting access to public methods

#### What is method overloading?

two methods with same name and different signatures, the proper one matching the usage will run

#### What is method overriding?

an inherited class overrides method wth same name/signature, and the one that overrides it runs.

#### Explain how object oriented languages attempt to simplify memory management for Programmers.

Garbage collector. It checks if a variable is still referenced through the program, and saves the allocated memory.

#### Explain the “Single Responsibility” principle!

A class should have only one reason to change. A class should solve one problem, but that problem fully.

#### What is an object oriented program? Explain, show.

We write program in objects, we use methods throguh objects and fields.

Object a = new Object();
a.callAMethod();
System.out.println(a.property);


#### How do you make a class immutable? What do you need to watch out for?

Declare the class as final so it can't be extended.
Make all fields private so that direct access is not allowed.
Don't provide setter methods for variables.
Make all mutable fields final so that its value can be assigned only once.
Initialize all the fields via a constructor performing deep copy.
Perform cloning of objects in the getter methods to return a copy rather than returning the actual object reference.

#### How many instances can be created for an abstract class?

none

## Programming languages

### Java

#### What is autoboxing and unboxing? 
Autoboxing: the java compiler converting primitive types to their reference selves. If the conversion goes the other way, this is called unboxing.
#### If you have a variable, that shall store a positive whole number between 0 and 200, what primitive type would you use to store it?

int. short would be better because it can contain numbers from -32768 to +32767, but more programmer knows int so I would adapt

#### What is the "golden rule" of variable scoping in Java? What is the lifetime of variables?

The golden rule is that static code cannot access non-static members by their simple name

#### What is the purpose of the ‘equals()’ method?

It compares objects by property values, not memory addresses

#### What is the difference between '==' and 'equals()'?

equals compares objects by property values, == by memory addresses. Primitive values are the same with both

#### What does the ‘static’ keyword mean?

it means that the variable/method is handled on a class basis. It can be altered, but if you alter it with different instances, then it will alter for all instances.

#### Why is the main() method declared as static? Explain.

Because it is directly called by the JVM without creating an object of the class in which it is declared. When java runtime starts, there is no object of class present.
JVM can this way just start the main method, and not allocating it memory.

#### What is the default access modifier in a class?

package-private, which means that all members are visible within the same package

#### What is the JVM?

Java virtual machine, which runs java programs. It allows java to be multiplatform

#### What is the difference between the JRE and the JDK?

Runtime environment and developer kit - one runs the program, the other compiles it and runs it.

#### What is the difference between long and Long?

long is a primitive type thus must have a value, Long is reference type thus can be null.

#### Can a long store bigger numbers than a Long?

No.

#### What kind of packages do you know under java.util.* ? Bring at least 3 examples.
List
Comparator
HashMap

#### What are the access modifiers in Java? Which one could we use for class?
class --> public

protected
private

#### Can an “enum” contain methods in Java? Explain.

yes. It is a class like any other. You can use a method to give real value to enum values.

#### When would you use a private/protected/public attribute? What is the difference?

private is valid in a "package" like a class- it is for exclusive fields/methods that only the class uses.
protected is like private but subclasses also use it.
public is that everyone has access to.

#### How do you prevent developers from subclassing a class?

using the final keyword

#### How do you prevent developers from overriding a method in a subclass?

1. using the static keyword
2. using the final keyword
3. using the private access modifier

#### How do you prevent developers from changing the value of a variable?

using the final keyword. Although it would mean at reference types that the fields/values inside are still changable.
We would need to make that class immutable to prevent that, and that would mean:
Declare the class as final so it can't be extended.
Make all fields private so that direct access is not allowed.
Don't provide setter methods for variables.
Make all mutable fields final so that its value can be assigned only once.
Initialize all the fields via a constructor performing deep copy.
Perform cloning of objects in the getter methods to return a copy rather than returning the actual object reference.

#### Think about money ;) How would you store a currency value, that shall support decimal parts? Think it through again, and try to think outside of the box!

I would store it in String. It is immutable, so security is a plus. If we would store it in double, how would we know what type of currency that is? Yuan? Dollars? Zloty? This way we can keep track of type. 
Also we could create a class system.
Money - abstract base class.
Dollar - subclass. and so on. We could keep track of the current sign for that money, or the current value on a base credit system.

#### What happens if you try to call something, that you have no access to, because of data hiding?

compile error, it fails to resolve symbol, because it doesnt recognize what it mustn't

#### What happens if you try to delete/drop an item from an array, while you are iterating over it?

it runs perfectly, because it is a static length container

#### What happens if you try to delete/drop/add an item from a List, while you are iterating over it?

it runs to error, because it is dynamic lengthed container and if you iterate on the 10th element when there is 9 then it is a problem

#### What happens if you try to add an item to the end of an array, while you are iterating over it?

Then why am I iterating over it if i try to add one to the END?

#### If you need to access the iterator variable after a for loop, how would you do it?

I would declare it outside the loop.

#### Which interfaces extend the Collection interface in Java. Which classes?

Iterable

List
Set
Queue
SortedSet
Deque
NavigableSet

#### What is the connection between equals() and hashCode()? How are they used in HashMap?

The basic rule of the contract states that if two objects are equal to each other based on equals() method, then the hash code must be the same.

In HashMap, hashCode() is used to calculate the bucket and therefore calculate the index. equals method is used to check that 2 objects are equal or not.

#### What is the difference between checked exceptions and unchecked exceptions? Could you bring example for each?

A checked exception is caught at compile time whereas a runtime or unchecked exception is, as it states, at runtime
A checked exception must be handled either by re-throwing or with a try catch block, whereas an unchecked isn't required to be handled.

#### What is Error in Java and how does it relate to Exception?

Exceptions and errors both are subclasses of Throwable class. The error indicates a problem that mainly occurs due to the lack of system resources and our application should not catch these types of problems

#### When does 'finally' block run? What it is used for? Could you give an example from your projects when you would use 'finally'?

EveryTime, it doesnt matter if we caught an exception or not. It is use to let the program run normally no matter what exception happens.
I would have used it in a webshop, when i want to ensure that no matter what parameter the users write in the query parameters it will give feedback to the user

#### What is the largest number you can work with in Java?

2147483647

#### When you use method overriding, can you change the access level of the method, from protected to public? Why?

Yes, because protected is a stricter modifier and you can always widen the access modifier, if it is still valid in the inheritance. Lets say you have a method protected communicate in LivingThings and you have public communicate in Dogs.
You ordered dog to be callable to communicate, while Not all animals can be comunicated at.

#### Can the main method be overridden? Explain your answer!

No, we cannot override main method of java because a static method cannot be overridde

#### When you use method overriding, can you throw fewer exceptions in the subclass than in the parent class? Why?

No, because it is in the signature, you cannot take anything from the signature.

#### When you use method overriding, can you throw more exceptions in the subclass than in the parent class? Why?

Yes, because it doesnt violate the signiture

#### What does "final" mean in case of a variable, method or a class?

in a variable that you cannot alter its memory address.
a final method cannot be overriden in the subclasses.
a final class cannot be inherited by other classes

#### What is the super keyword?

it call the inherited classes method/variable/constructor

#### What are “generics”? When to use? Show examples.

when after a class name  there is <T>, which is good if you want to use your class with different value types.
for example List<String>

#### What is the benefit of having “generic” containers?

Because this way you can store several types in one written class

#### Given two Java programs on two different machines. How can you communicate between the two? What are the possible ways?

POST/GET/PUT/DELETE HTTP requests

Or you could set a remote database/file that is accessible by the two programs, and you write in that file by the two programs, then they communicate indirectly

#### What is an annotation? What can be annotated and how? Show examples.

A form of metadata. They have no direct effect on the operation of the code. They can be used to detect compile errors, or warnings, to generate code, or to be examined through runtime. 
Classes, methods, variables, parameters and Java packages may be annotated

### C&#35;

#### Explain the purpose of IL and how does it relate to CLR?
#### What does “managed code” mean?
#### What is an assembly?
#### What is the difference between an EXE and a DLL?
#### What is the difference between `dotnet build` and `dotnet restore`?
#### What is strong-typing versus weak-typing? Which is preferred? Why?
#### What is a namespace?
#### Explain sealed class in C#?
#### What is explicit vs. implicit conversion? Give examples of both of them.
#### Is a struct stored on the heap or stack?
#### Can a struct have methods?
#### Can DateTimes be null?
#### List out the differences between Array and ArrayList in C#?
#### How is the using() pattern useful? What is IDisposable? How does it support deterministic finalization?
#### How can you make sure that objects using dedicated resources (database connection, files, hardware, OS handle, etc.) are released as early as possible?
#### Why to use keyword “const” in C#? Give an example.
#### What is the difference between “const” and “readonly” variables in C#?
#### What is a property in C#?
#### List out two different types of errors in C#?
#### What is the difference between “out” and “ref” parameters in C#?
#### Can we override private virtual method in C#?
#### What's the difference between IEquatable and just overriding Object.Equals()?
#### Explain the differences between public, protected, private and internal. Explain access modifier – “protected internal” in C#!
#### What’s the difference between using `override` and `new` keywords when defining method in child class?
#### Explain StringBuilder class in C#!
#### How we can sort the array elements in descending order in C#?
#### Can you use a value type as a generic type argument in C#? For example when implementing an interface like (IEquatable).
#### What are Nullable Types in C#?
#### Conceptually, what is the difference between early-binding and late-binding?
#### What is delegate, event, callback, multicast delegate?
#### What is enum in C#?
#### What is null-conditional operator?
#### What is null-coalescing operator?
#### What is serialization?
#### What is the difference between Finalize() and Dispose() methods?
#### How do you inherit a class from another class in C#?
#### What is difference between “is” and “as” operators in C#?
#### What are indexers in C# .NET?
#### What is the difference between returning IQueryable<T> vs. IEnumerable<T>?
#### What is LINQ? Explain the idea of extension methods.
#### What are the advantages and disadvantages of lazy loading?
#### How to use of “yield” keyword? Mention at least one practical scenario where it can be used?
#### What are attributes in C#? Give some examples of usage of them.
#### By what mechanism does NUnit know what methods to test?
#### What is the GAC? What problem does it solve?
#### What is the largest number you can work with in C#?
