

f-from-c.e: c-main.o f-sum.o
	gcc c-main.o f-sum.o -o f-from-c.e

c-main.o: c-main.c
	gcc -c c-main.c -o c-main.o

f-sum.o:
	gfortran -c f-sum.f90 -o f-sum.o
