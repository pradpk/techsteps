Java SE - Java Standard Edition, Java EE - Java Enterprise Edition


Object Oriented Concepts
------------------------------------
1. Abstraction: In Java, abstraction is hiding certain details and showing essential features of the object. It lets users to focus on capabilities of the object, not on how it does. 
2. Encapsulation: This deals with the state of the object. Objects encapsulate their state and users of object can access through functions or methods. Example is classes having variables with private modifiers and expose their state using getter and setter.
3. Inheritance: Java allows classes to inherit state and behavior from other classes. Each class is allowed to have only one superclass and each superclass can have unlimited subclasses.
4. Polymorphism: expressing in different forms or behaviors. Subclasses of a class can define their own unique behaviors by overriding the method with their own implementation.
5. Class: blueprint or prototype of object which defines its state and behavior.
6. Interface: It is a contract where anybody implementing an interface needs to provide the behavior.


Pass By Value
--------------------
Java passes the arguments by value. 
When you send primitive data as an argument to a method, any changes in the value of the parameter will exist only within the scope of the method. When the method returns, any changes to them are lost. 
When you send an object to a method, JVM passes the object reference to the method. Values of the object’s fields can be changed if they have proper access level and it will still be reflected outside of the method. If you create a new reference for the object within the method, object reference will not be changed outside the method. 

HashMap
-----------
-  Initial capacity of hashmap is number of buckets in hash table. When the load factor reaches 75% (12), the size of the hashmap is doubled by recomputing its hashcode of existing data structure elements. We can create HashMap with initial capacity and load factor. Hashmap stores the object as key-value pair. 
- It stores the data in the bucket and labels the bucket with the hash of the key. Hashmap uses Array and LinkedList data structure to achieve this. 
- It is similar to Hashtable except that it is unsychronized and permits null key and null values.

