CC=gcc

WARN=-Wall
OPTIMIZATION=-O2
DEBUG=-g
CFLAGS=-I../

LDCFLAGS= -L../
LIBS=-lsoprint

TARGET=test
OBJECT=test.o


$(TARGET):$(OBJECT)
	$(CC) -o $@ $^ $(LDCFLAGS) $(LIBS)

%.o:%.c
	$(CC) $(WARN) $(OPTIMIZATION) $(DEBUG) $(CFLAGS) -c $< -o $@

.PHONY:
	clean
clean:
	rm -rf $(TARGET) $(OBJECT)
