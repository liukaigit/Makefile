CC=gcc

# -Wall : all types of the alarm information
# -g 	: gdb debugging information
# -O2	: code optimization
WARN=-Wall
OPTIMIZATION=-O2
DEBUG=-g

# other compiler options
CFLAGS=-I../

# the static library path and dependent libraries
LDCFLAGS=-L../
LIBS=-laprint

TARGET=test
OBJECT=test.o

$(TARGET):$(OBJECT)
	$(CC) -o $@ $^ $(LDCFLAGS) $(LIBS)

%.o:%.c	
	$(CC) $(WARN) $(OPTIMIZATION) $(DEBUG) $(CFLAGS) -c $^ -o $@

.PHONY:
	clean

clean:
	-rm -rf $(TARGET) $(OBJECT)
