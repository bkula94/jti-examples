CC=gcc
CFLAGS=-c -fPIC -I${JAVA_HOME}/include
DEPS = HelloWorldJNI.h
OBJ = HelloWorldJNI.o

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

HelloWorldJNI: $(OBJ)
	$(CC) -dynamiclib -o libnative.dylib HelloWorldJNI.o -lc

HelloWorldJNI.h: HelloWorldJNI.java
	javac -h . HelloWorldJNI.java

.PHONY: clean
clean:
	rm -f HelloWorldJNI.h *.class *.o libnative.dylib
