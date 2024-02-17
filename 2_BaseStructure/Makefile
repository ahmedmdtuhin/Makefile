#Targets
#Pattern is : targen_name: prerequisites or dependencies then commands(lists)
#The prerequisities are names and separated by spaces.
build: my_lib.o main.o 
	g++ main.o my_lib.o -o main

main.o:
	g++ main.cc -c 
#g++ main.cc -c main.o


my_lib:
	g++ my_lib.cc -c 
#g++ my_lib.cc -c my_lib.o

execute:
	./main

clean:
	rm -f *.o
	rm -f main
