README.md

sudo apt install chicken-bin

Para comprobar el funcionamiento de la función que calcula el 
máximo común divisor usando Scheme hay dos alternativas:

1) Ejecutar el script directamente puesto que incluye el sbang:
   ./gcd.smc
   
   Dando previamente permisos de ejecución: chmod u+x gcd.scm

2) Invocar al intérprete de Scheme (llamdo Chicken) y hacerlo de forma
   interactiva usando el REPL (Read-Eval-Print Loop):
   $csi

CHICKEN
(c) 2008-2013, The Chicken Team
(c) 2000-2007, Felix L. Winkelmann
Version 4.8.0.5 (stability/4.8.0) (rev 5bd53ac)
linux-unix-gnu-x86-64 [ 64bit manyargs dload ptables ]
compiled 2013-10-03 on aeryn.xorinia.dim (Darwin)

#;1> (load "gcd.scm")         
; loading gcd.scm ...
1
#;2> (print (eval( gcd 5 7)))
1
#;3> ,q

Para salir escribir una coma seguida de una q(uit)


El enlace a la página de Chicken es:
http://wiki.call-cc.org/man/4/Getting%20started

