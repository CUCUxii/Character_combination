# Character_combination
Script en Python que hace todas las combinacione posibles de caracteres dados en una lista sin repetir ninguno


Este script lo hice cuando vi a un familiar jugar a un juego de combinar letras para formar palabras.
  Al usuario se le piden los caracteres y de ahi sale una lista, (ejemplo cinco letras), el algoritmo tiene que 
  combinarlas sin repetir elementos de la lista (si hay una "r" pues una r, si hay dos, dos, no tres ni cuatro)
  Las combinaciones son de la longitud de la serie de letras hasta tres caracteres solo.
  
Se me ocurrió hacer
un algoritmo que hiciera el trabajo por ti. 
La parte facil era lo de hacer las combinaciones, la parte dificil, la de que no se repitieran caracteres en una lista 
más de lo indicado.

Al principio pensé en sacar el decimal de cada letra de la lista con la función "ord(letra)" y sumarlos todos.
(Con las letras "p", "e", "r", "r", "o" si haces el ord de todos y lo sumas da 520). Es el resultado de sumar ese numero
exacto de letras, sin repetir otras. Por tanto de todas las combinaciones, sacar el ord de sus letras, sumarlo y compararlo
con "520", las que den 520 son las validas y las que no no (ejemplo "Perro" y "Epro" dan 520)
Eso sin saber que numero va a dar porque cada vez el usuario daria letras disitntas
  Haria una lista por tanto de letras y cada vez que se añadiera una combinacion se calcula y se añade al menos que ya 
  se haya añadido antes. 
  
Parecia una buena idea pero tiene las desventajas de que el primer elemento que tenga 520 aunque sea valido, por ser
el primero no saldria en la lista. 

Despues de devanarme los sesos buscando funciones llegue a la conclusion de que era mejor tirar de diccionaios:
  Habria que crear un diccionario que contara las veces que salia cada letra en la lista (P:1, e:1, r:2, 0:1)
  y compararlo con cada una de las combinaciones. Las combinaciones de cinco o menos letras que tengan ese numero o menor 
  (en caso de "pero", hay una sola "r") son las válidas

  Ej -> Si pones "Perro" tiene que haber una "p" y dos "r" no tres ni cuatro.

Aunque sea un programa un poco absurdo, ha sido un ejercicio entretenido de programación, y añadiendole algunas cosas al 
script se puede hacer un programa para crear claves de producto o algo del estilo.
