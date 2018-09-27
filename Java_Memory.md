Java Heap and its Size
Java Virtual machine is a “virtual” execution engine instance that executes the bytecodes in Java class on a microprocessor. Java heap is where the objects of a Java program live. It is the repository of live, dead objects and some free memory. 
-Xmnsize – Initial and max size of heap for young generation (new objects). Oracle recommends to keep the size between a half and a quarter overall heap size.
-Xmssize – Initial size of the heap (must be multiple of 1024 and greater than 2 MB).
-Xmxsize – Max size of the heap

Java Memory Management
Prior to Java 8, memory in Java was split into heap and non-heap space, In Java, we have Objects and Classes 
(Objects are instantiations of Classes). 
Object data is stored on heap space, class data is stored on non-heap space (permanent generation or PermGen).
Class data will consist of name of class, methods, fields, object arrays and type arrays associated with class. 
PermGen also has JVM’s internal objects and compiler information.
Java 8 replaces PermGen with MetaSpace. PermGen used to be in touch with heap data, but MetaSpace is held in native memory. 

Java Heap Size and Garbage Collection
When an object can no longer be reached from any pointer in the running program, it is considered to be garbage collected.  One of the best practice is to tune the time spent doing the garbage collection to within 5% of execution time. 
JVM heap size determines how often VM spends on garbage collection. Setting a large heap size makes garbage collection slower and less frequent. Optimum way is to set heap size in accordance to your memory needs.
Goal of tuning heap size is to minimize JVM spending time on garbage collection while increasing the number of clients served. 

Java Object Memory Management
Every Java object in memory has 2 areas: header area and data area. Header area contains details like pointer to object class, 
garbage collection status, hash code, lock fields, age information, length of the array etc. Data area contains the values of all 
instance variables. Header area layout is fixed for a particular JVM implementation (e.g. uses 2/3 machine words (3 words if an array, 
1 word is 4 bytes in 32 bit architecture)). Data area is dependent on the object layout.

Garbage Collection Terminology
•	Dangling reference is a reference in memory that is already reclaimed but still being referenced by a program. Example, two modules m1 and m2 uses reference r1, but m2 accidentally reclaims the memory referenced by r1, but m1 can try to use r1.
•	Memory leak is a reference in memory where the reference is not used but not reclaimed. Example, two modules m1 and m2 uses reference r1, and both of them don’t reuse them, but never reclaim the memory. Excessive memory leaks will make the program run out of memory.
•	Dead object or garbage is an object that cannot be used by running program in future. Opposite is live object.
Heap size tuning
Determination of proper JVM heap size can be done by considering below parameters. 
•	How many different applications will be deployed to single JVM process (number of EAR/WAR/JAR)
•	How many Java classes will be potentially loaded at runtime, including third party APIs
•	Estimation of in-memory caching footprint (internal cache structures defined by third party APIs and cached data from database/file)
•	Estimation of number of threads used by application
