

c-from-f.e: c-sum.o f-main.o
	gcc c-sum.o f-main.o -lgfortran -o f-from-c.e

c-sum.o: c-sum.c
	gcc -c c-sum.c -o c-sum.o

f-main.o: f-main.f90
	gfortran -c f-main.f90 -o f-main.o
