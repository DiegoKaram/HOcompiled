

suma.e : sum-cpp.o c-main.o
	g++ sum-cpp.o c-main.o -o suma.e

sum-cpp.o: cpp-sum.cpp
	g++ -c cpp-sum.cpp -o sum-cpp.o
c-main.o: c-main.c
	g++ -c c-main.c -o c-main.o
