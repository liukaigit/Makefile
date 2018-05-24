CC=gcc
# compiler options
# -Wall : all types of the alarm information
# -O2	: code optimization
# -g	: gdb debugging information
WARN=-Wall
OPTIMIZATION=-O2
DEBUG=-g
CFLAGS=-fPIC

# the dynamic library path
LDFLAGS=
LIBS=

TARGET=libsoprint.so
OBJECT=soprint.o printso.o

# other process calls
OUTPUT_INCLUDE=soprint.h
OUTPUT_LIB=$(TARGET)

# the installation path
INSTALL_INCLUDE_PATH=../include
INSTALL_LIB_PATH=../lib

# test case
TESTCASE=example

$(TARGET):$(OBJECT)
	$(CC) -shared $^ -o $@
	make  -C $(TESTCASE)

%.o:%.c
	$(CC) $(WARN) $(OPTIMIZATION) $(CFLAGS) -c $^ -o $@

#install:
#	cp -rf $(OUTPUT_INCLUDE) $(INSTALL_INCLUDE_PATH)
#	cp -rf $(OUTPUT_LIB) $(INSTALL_LIB_PATH) 
#
#uninstall:
#	rm -rf $(INSTALL_INCLUDE_PATH)/$(OUTPUT_INCLUDE)
#	rm -rf $(INSTALL_LIB_PATH)/$(OUTPUT_LIB)

clean:
	-rm -rf $(OBJECT) $(TARGET)
	make clean -C $(TESTCASE)

.PHONY:clean install uninstall
