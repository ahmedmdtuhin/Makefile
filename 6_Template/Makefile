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
#EXECUTABLE_NAME = main
INCLUDE_DIR = inc
SOURCE_DIR = src
BUILD_DIR =build

CXX_STANDARD = c++17
CXX_WARNINGS =-Wall -Wextra -Wpedantic
CXX = g++
CXXFLAGS =$(CXX_WARNINGS) -std=$(CXX_STANDARD)
#I incdicates where the complier should look for include files, task of a preprocessor
CPPFLAGS = -I $(INCLUDE_DIR)
LDFLAGS = #-lmath

ifeq ($(DEBUG), 1)
CXXFLAGS += -g -O0
EXECUTABLE_NAME =mainDebug
else
CXXFLAGS += -O3
EXECUTABLE_NAME =mainResease
endif

COMPILER_CALL = $(CXX) $(CXXFLAGS) $(CPPFLAGS)

#wildcard is a function that will give the list of all source files with .cc extention
CXX_SOURCES = $(wildcard $(SOURCE_DIR)/*.cc)
#patsubst function substitutes everything ends with .cc and substitutes with .o files based on the given list
#patsubst : $(text:pattern=replacement)
CXX_OBJECTS = $(patsubst $(SOURCE_DIR)/%.cc, $(BUILD_DIR)/%.o, $(CXX_SOURCES))



build: $(CXX_OBJECTS)
	echo $(CXX_SOURCES)
	$(COMPILER_CALL) $(CXX_OBJECTS) $(LDFLAGS) -o $(BUILD_DIR)/$(EXECUTABLE_NAME)

#main.o:
#$(COMPILER_CALL) main.cc -c 
#g++ main.cc -c main.o


#my_lib:
#$(COMPILER_CALL) my_lib.cc -c 
#g++ my_lib.cc -c my_lib.o

execute:
	./$(BUILD_DIR)/$(EXECUTABLE_NAME)  

clean:
	rm -f $(BUILD_DIR)/*.o
	rm -f $(BUILD_DIR)/$(EXECUTABLE_NAME) 

#PATTERNS(Template)
# $@: File name of the target
# $<: Name of the first dependency
# $^: Name of all prerequisites

$(BUILD_DIR)/%.o: $(SOURCE_DIR)/%.cc
	$(COMPILER_CALL) -c $< -o $@    

#ALias:
# main.o: main.cc
# $(COMPILER_CALL) -c main.cc -o main.o 

#Others extentions
#%.o: %.pp
#$(COMPILER_CALL) -c $< -o $@  

#%.o: %.cxx
#$(COMPILER_CALL) -c $< -o $@  


