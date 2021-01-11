# Expresiones, Filtros y Calculando Valores con QGIS 2.18
Video de youtube del taller:
https://www.youtube.com/watch?v=hkfy4XALPfc
##
## ¿Qué es una expresión? 

*[1]* En un lenguaje de programación es una combinación de uno o más valores explícitos, constantes, variables, operadores y funciones que interpreta el lenguaje de programación (de acuerdo con sus reglas particulares de precedencia y de asociación y calcula para producir ("para devolver") , en un entorno con estado otro valor.  Este proceso, como para las expresiones matemáticas, se llama evaluación.

*[2]* Cualquier parte del código del programa en un lenguaje de alto nivel que, cuando (si) su ejecución finaliza, devuelve un valor.  En la mayoría de los lenguajes de programación, las expresiones constan de constantes, variables, operadores, funciones y paréntesis.  Los operadores y las funciones pueden estar integrados o definidos por el usuario.  

## Componentes de una expresión:

**Constantes:** Un valor que no puede ser alterado por el programa durante la ejecución normal, es decir, el valor es constante. Geometría y dato original.
**Valores:** Es la representación de alguna entidad que puede ser manipulada por un programa.  Geometría (área, distancia, ubicación, etc) y datos dentro de la geometría (población, temperatura, etc)
**Variable:** Es una ubicación de almacenamiento (identificada por una dirección de memoria) emparejada con un nombre simbólico asociado (un identificador), que contiene cierta cantidad de información conocida o desconocida denominada valor. El nombre de la variable es la forma habitual de referenciar el valor almacenado, además de referirse a la variable en sí, dependiendo del contexto.
Resultado
**Función (Rutina):** Una secuencia de instrucciones de programa que realizan una tarea específica.
**Operadores:** Permiten construcciones que se comportan generalmente como funciones, pero que difieren sintáctica (conjunto de reglas) o semánticamente (Significado de las combinaciones) de las funciones habituales.

## ¿Para qué nos sirven las expresiones en QGIS?

*[3]* Es una forma poderosa de manipular el **valor de atributo, la geometría** y **las variables** para cambiar dinámicamente el estilo geométrico, el contenido o posición de la etiqueta, el valor del diagrama, la altura de un elemento del compositor, seleccione algunas características, cree un campo virtual ..

## Los operadores en QGIS ......(Query Builder)

El ***generador de cadenas expresiones*** está disponible en muchas partes en QGIS y particularmente, se puede interactuar cuando veamos el símbolo sigma, ejemplos:

 - Panel de estadísticas
![Simbolo Sigma](https://docs.qgis.org/3.4/en/_images/mIconExpression.png)
 - Selección por expresiones
![enter image description here](https://docs.qgis.org/3.4/en/_images/mIconExpressionSelect.png)
 - Calculadora
 ![enter image description here](https://docs.qgis.org/3.4/en/_images/mActionCalculateField.png)
 - Elaboración de simbología mediante datos
![enter image description here](https://docs.qgis.org/3.4/en/_images/mIconDataDefine.png)
 - Caja de calculadora de campos

![enter image description here](https://docs.qgis.org/3.4/en/_images/function_list.png)


## Filtrado y cálculo de valores 
QGIS tiene cierto soporte para el análisis de expresiones similares a SQL.  Solo se admite un pequeño subconjunto de sintaxis SQL.  Las expresiones se pueden evaluar como predicados booleanos (devolviendo True o False) o como funciones (devolviendo un valor escalar).  Consulte Expresiones en el Manual del usuario para obtener una lista completa de las funciones disponibles.
Tres tipos básicos son compatibles:
número - tanto números enteros como decimales, p. ej. `123` , `3.14`
cadena - tienen que estar entre comillas simples: `'hola mundo'`
referencia de columna: al evaluar, la referencia se sustituye por el valor real del campo.  Los nombres no son escapados.
Las siguientes operaciones están disponibles:
operadores aritméticos: `+ , - , * , / , ^`
paréntesis: para imponer la precedencia del operador: `(1 + 1) * 3`
unario más y menos: `-12 , +5`
funciones matemáticas: `sqrt , sin , cos , tan , asin , acos , atan`
funciones de conversión: `to_int , to_real , to_string , to_date`
funciones de geometría: `$ area` , `$ length`
funciones de manejo de geometría: `$ x` , `$ y` , `$ geometry` , `num_geometries` , `centroid`
Y los siguientes predicados son compatibles:
comparación: `=` ,`! =` , `>` , `> =` , `<` , `<=`
coincidencia de patrón: `LIKE (usando% y _)`, ~ `(expresiones regulares)`
predicados lógicos: `and` , `or` , `not`
Comprobación de valores `NULL`,`IS NULL` , `IS NOT NULL`
Ejemplos de predicados:

    1 + 2 = 3

    sin (ángulo) > 0

    'Hola' i like 'He%'

    (x > 10 AND y > 10) O z = 0

Ejemplos de expresiones escalares:

     - `2 ^ 10`
     - sqrt (val)
     -  $ length + 1
## Lista de "funciones en QGIS"

![enter image description here](https://docs.qgis.org/3.4/en/_images/customFunction.png)


**Lista completa:**
https://docs.qgis.org/3.4/en/docs/user_manual/working_with_vector/expression.html?highlight=field%20calculator

**Referencias:**
[1]
https://en.wikipedia.org/wiki/Expression_(computer_science)
[2]
http://foldoc.org/Expression
[3]
https://docs.qgis.org/2.18/es/docs/user_manual/working_with_vector/expression.html#vector-expressions


**Tema de los datos :
¿Qué tan cerca esta una gasolinera de una escuela?**

https://datos.gob.mx/busca/dataset/catalogo-de-centros-de-trabajo-de-sep

Datos de gasolineras: 
http://datamx.io/dataset/estaciones-de-servicio-pemex-2017

Gracias por su atención. 
