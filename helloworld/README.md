# This basic JNI example calls c from java to print hello world.
This example differs only slightly from https://www.baeldung.com/jni. It adds a makefile and uses c instead of c++.

### Dependencies
* JAVA_HOME is set
* gcc is on path, this could be replaced with g++ in the makefile

### To run
cd into the directory make the executable with
```
make
```
run with
```
java HelloWorldJNI
```
