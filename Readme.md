README.md

El objetivo es crear los ficheros intermedios del proceso de compilación
en C y ver lo que produce el ensamblador.

Los pasos para crear una biblioteca estática (static library) son:

1.-) Crear un fichero C que contenga las funciones de nuestra biblioteca:

El fichero 'gdc.c' contiene el código para calcular el
Máximo común divisor a través del algoritmo iterativo de euclides.

2.-) Crear un fichero de cabecera para la biblioteca.
El fichero 'gdc.h' contine la declaración de la función para calcular el
Máximo común divisor a través del algoritmo iterativo de euclides.

3.-) Compilar los ficheros de la biblioteca

gcc -c gcd.c -o lib_mylib.o

4.-) Crear una biblioteca estática.
El comando 'ar' empaqueta múltiples ficheros objeto en un única biblioteca
estática. La salida de este comando es una biblioteca estática.

ar rcs lib_mylib.a lib_mylib.o

5.-) La biblioteca está lista para ser usada. Se puede copiar lib_mylib.a en
cualquier parte para ser usada, por ejemplo, se puede dejar en el directorio 
actual:
   a.-) Se crea un fichero C on la función principal con un llamada a la 
        función de la biblioteca.
        
        El fichero 'main.c' incluye la cabecera e invoca a la función creada.
       
   b.-) Compilar el programa de prueba:
   
        gcc -c main.c -o main.o

   c.-) Enlazar el fichero principal con la biblioteca estática 
        (la opción -L indica el camino donde buscar y 
         la opción -l le dice al enlazador el nombre la biblioteca a usar.
         
        gcc -o main main.o -L. -lmylib
        
   d.-) Ejecutar el main
   
        ./main
        

Para obtener los ficheros intermedios utilizar:

Compile to assembly code: gcc -c -g -S gcd.c 
Disassembly: objdump -S --disassemble gcd.o > gcd.dump

Augmented code: gcc -c -g -Wa,-a,-ad  gcd.c > gcd.lst
