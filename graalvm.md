
- GraalVM offers a comprehensive platform in which an application can be developed with multiple programming languages including Java, Javascript, Ruby, Python, R, C/C++.
- Java applications will run faster in GraalVM than JVM (terms and conditions apply) which will be benefical in addition to providing extensibility via scripting languages.
- To take advantage of GraalVM, we can create native images from JVM based applications and run the image (ahead of time compilling). This will reduce the startup costs. Example to build native image : https://www.graalvm.org/docs/examples/native-list-dir/
- As part of ahead of time compilation, we create native images for the application, then Java program inside the application doesn't run on Java HotSpot VM, but uses memory management and thread scheduling and runs on Substrate VM (which is already compiled into native executable). This is the reason behind Java's quick start up compared to JVM. This should be done for applications which need quick startup and less memory footprint as there are few features that are not supported - https://github.com/oracle/graal/blob/master/substratevm/LIMITATIONS.md

