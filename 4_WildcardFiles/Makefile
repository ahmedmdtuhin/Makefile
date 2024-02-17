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


CXX_OBJECTS = my_lib.o main.o 

build: $(CXX_OBJECTS)
	$(COMPILER_CALL) $(CXX_OBJECTS) $(LDFLAGS) -o $(EXECUTABLE_NAME)

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

#PATTERNS(Template)
# $@: File name of the target
# $<: Name of the first dependency
# $^: Name of all prerequisites

%.o: %.cc
	$(COMPILER_CALL) -c $< -o $@    

#ALias:
# main.o: main.cc
# $(COMPILER_CALL) -c main.cc -o main.o 

#Others extentions
#%.o: %.pp
#$(COMPILER_CALL) -c $< -o $@  

#%.o: %.cxx
#$(COMPILER_CALL) -c $< -o $@  


