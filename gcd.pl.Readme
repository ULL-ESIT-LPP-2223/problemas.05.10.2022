cd(A,B,G) :- A = B, G = A.
gcd(A,B,G) :- A > B, C is A-B, gcd(C,B,G).
gcd(A,B,G) :- B > A, C is B-A, gcd(C,A,G).

En un lenguaje de programación lógica el programador
especifíca un conjunto de axiomas y reglas de prueba
que permiten al sistema encontrar el valor deseado.

La proposición mcd(a,b,g) es cierta si:

(1) a, b y g son todos iguales
(2) a es mayor que b y existe un número c tal que c es a-b y
    mcd(c,b,g) es cierto o
(3) a es menor que b y existe un número c tal que c es b-a y
    mcd(c,a,g) es cierto

Para calcular el mcd de un par de números dados,
buscar un número g (y varios números c) para los cuales
estas reglas permitan probar que mcd(a,b,g) es cierto.
