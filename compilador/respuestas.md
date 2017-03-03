#Respuestas

##Primer punto
1. Al ejecutar `preprocessing` espero que interprete la informacion contenida en
los headers (y otras definiciones) para ser reemplazada en el codigo, en un
archivo nuevo.
2. La primera etapa de compilacion traduce el codigo generado por el
preprocesador a lenguaje assembler.
3. En la segunda parte de la compilacion, el codigo assembler generado en la
primera parte e traduce a lenguaje de maquina
4. En el ultimo paso se linkean todas las partes del ejecutable, como las que
 estan en el codigo de calculator con las de las librerias usadas.

##Segundo punto
Al ejecutar `make preprocessing` se crea un archivo nuevo que contiene las
todas las """"""""""""""definiciones"""""""""""""""" de los headers, junto con
lo escrito en  el codigo de `calculator.c`.   

##Tercer punto
En el codigo de assembler se encuentran las siguientes lineas que parecen ser
una definicion de la funcion `add_numbers`:
```
add_numbers:
.LFB1:
	.cfi_startproc
	push	rbp
	.cfi_def_cfa_offset 16
	.cfi_offset 6, -16
	mov	rbp, rsp
	.cfi_def_cfa_register 6
	mov	DWORD PTR [rbp-4], edi
	mov	DWORD PTR [rbp-8], esi
	mov	eax, DWORD PTR [rbp-8]
	mov	edx, DWORD PTR [rbp-4]
	add	eax, edx
	pop	rbp
	.cfi_def_cfa 7, 8
	ret
	.cfi_endproc
.LFE1:
	.size	add_numbers, .-add_numbers
	.ident	"GCC: (Ubuntu 4.8.4-2ubuntu1~14.04.3) 4.8.4"
	.section	.note.GNU-stack,"",@progbits
```
##Cuarto punto
Al generarse lo objetos, miramos los simbolos que tiene usando `nm`
encontramos el simbolo `T` que representa una funcion visible desde otras
unidades al compilar, y el sibolo `U` que representa algo indefinido en
esta unidad.

##Quinto punto
A diferencia del objeto `calculator.o`, `calculator.e` tiene simbolos de cosas
locales, no visibles desde otras unidades y variables ,ademas de funciones y
cosas indefinidas.
