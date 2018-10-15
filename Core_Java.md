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
-  Initial capacity of hashmap is number of buckets in hash table. We can create HashMap with initial capacity and load factor. When the load factor reaches 75% (12), the size of the hashmap is doubled by recomputing its hashcode of existing data structure elements.
- It is similar to Hashtable except that HashMap is unsychronized and permits null key (once) and (multiple) null values. Hashtable will allow non-null object as key or value.
- Hashmap has 2 methods mainly - put and get. Put method gets the hash code of the key and identifies the bucket where Entry object will be stored. Hash collision occurs if the bucket is already present. equals() method is used to find if the key already exists in the bucket. If found, value will be replaced. If not found, a new node (Entry object) is created with the same bucket (LinkedList data structure will be used). Get method will also calculate the hashcode of key  to identify the bucket to pull the Entry object.
- Java 8 uses balanced trees data structure instead of LinkedList to optimize within the bucket after a certain threshold is reached.
- Types : ConcurrentHashMap, ConcurrentSkipListHashMap, EnumMap, Hashtable, IdentityHashMap, LinkedHashMap, TreeMap, WeakHashMap.
- ConcurrentHashMap is a version of synchronized HashMap and recommended than Hashtable or Collections.synchronizedMap(HashMap). ConcurrentHashMap get and put are not synchronized and synchronizes only necessary portion which provides better performance. Hashtable provides synchronized get and put methods. 
- EnumMap for collections of enum types. All of the keys in EnumMap should come from single enum type. IdentityHashMap uses reference equality (k1==k2) instead of object equality (k1.equals(k2)) while comparing keys. LinkedHashMap uses linked list implementation with hash table.
- TreepMap is sorted (based on natural ordering and provides log(n) for get, put, remove and containsKey operations) Map implementation. ConcurrentSkipListMap provides concurrent implementation with SkipList type of ordering. It can be used for faster in-order traversal (but TreeMap is recommended for overall sorted map operations).


