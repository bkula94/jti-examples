CC=gcc
# CFLAGS=-I.
CFLAGS=-c -fPIC -I${JAVA_HOME}/include
DEPS = HelloWorldJNI.h
OBJ = HelloWorldJNI.o

%.o: %.c $(DEPS)
	$(CC) -c -fPIC -I${JAVA_HOME}/include HelloWorldJNI.c -o HelloWorldJNI.o
	# $(CC) -c -o $@ $< $(CFLAGS)

HelloWorldJNI: $(OBJ)
	$(CC) -dynamiclib -o libnative.dylib HelloWorldJNI.o -lc
	# $(CC) -o $@ $^ $(CFLAGS)
