#Targets
#Pattern is : targen_name: prerequisites or dependencies then commands(lists)
#The prerequisities are names and separated by spaces.

#FLAGS
#CC: for compiling C programs; default CC
#XX : Program for compiling C++ programs; default g++
#CFLAGS: Extra flags to give to the C comiler
#CXXFLAGS :Extra flags to give to the C++ comiler
#CPPFLAGS: Extra flags to give to the C preprocessor
#LDFLAGS : Extra flags to give to the linker

DEBUG =1
EXECUTABLE_NAME = main

CXX_STANDARD = c++17
CXX_WARNINGS =-Wall -Wextra -Wpedantic
CXX = g++
CXXFLAGS =$(CXX_WARNINGS) -std=$(CXX_STANDARD)
LDFLAGS = #-lmath

ifeq ($(DEBUG), 1)
CXXFLAGS += -g -O0
else
CXXFLAGS += -O3
endif

COMPILER_CALL = $(CXX) $(CXXFLAGS)




build: my_lib.o main.o 
	$(COMPILER_CALL) main.o my_lib.o $(LDFLAGS) -o $(EXECUTABLE_NAME)

main.o:
	$(COMPILER_CALL) main.cc -c 
#g++ main.cc -c main.o


my_lib:
	$(COMPILER_CALL) my_lib.cc -c 
#g++ my_lib.cc -c my_lib.o

execute:
	./main

clean:
	rm -f *.o
	rm -f main
