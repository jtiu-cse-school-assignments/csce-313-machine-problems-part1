# makefile

all: memtest

free_list.o : free_list.c free_list.h
	g++ -c -g free_list.c 

my_allocator.o : my_allocator.c my_allocator.h free_list.h
	g++ -c -g my_allocator.c 

memtest: memtest.c my_allocator.o free_list.o
	g++ -o memtest memtest.c my_allocator.o free_list.o
	

clean:
	rm *.o memtest