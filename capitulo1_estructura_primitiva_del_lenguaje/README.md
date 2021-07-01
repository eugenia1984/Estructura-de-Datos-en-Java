# CAPITULO 1 : ESTRUCTURA PRIMITIVA DEL LENGUAJE

## El código fuente actualizado dle libro se puede ver en: http://www.cs.fiu.edu/vweiss

## Para consultas del libro: www.aw.com/csssupport

El código fuente Java reside en archivos cuyos nombres terminan con el sufijo **.java** .<br>
El compilador local, **javac**, compila y genera archivos **.class**, que contienen código de bytes. <br>
El **código de bytes Java** represetna el lenguaje intermedio portable que luego será interpretado ejecutando el **intérprete de Java**. <br>
El intérprete de Java se conoce con el nombre de **Máquina virtual**.<br>

---


## PRIMER PROGRAMA

```
public class FirstPrograma {
  
   public static void main( String [] args) {
   
    System.out.println("Is there anybody out there?" );
   }
}
```

---


## COMENTARIOS

Comentario en línea:

```
//Esto es un comentario en linea
```

Comentario multilínea:

```
/* Esto es un comentario
de dos lineas */
```

Para utilizar JavaDOC, la cual generará la documentación del programa a partir de los comentarios:
```
/*
*
*/
```

Los comentarios facilitan la lectura del código y nos facilitan la comprensión del programa a nosotros mismos.


---

## MAIN

Un programa Java está compuesto por una colección de **clases** que interactúan, las cuales contienen una serie de **métodos**. <br<
El equivalente de Java de las funciones y procedimientos es el **método estático**. <br>
Al ejecutar cualquier programa se invoca el método estático **main**. <br>

## SALIDAS A TRAVES DE TERMINAL

**println** es el mecanismo de salida principal en Java.


---


## TIPOS PRIMITIVOS

Son de 8 tipos: <br>

**byte** | almacena: enteros de 8 bits | rango: -128 a 127 <br>

**short** | almacena: enteros de 16 bits | rango: -32.768 a 32.767 <br>

**int** | almacena: enteros de 32 bits | rango: -2.147.483.648 a 2.147.483.647 <br>

**long** | almacena: enteros de 8 bits | rango: -128 a 127 <br>

**float** | almacena: coma flotante de 32 bits | rango: 6 digitos significativos (decimales) <br>

**double** | almacena: coma flotante de 64 bits | rango: 15 digitos signifiativos (decimales) <br>

**char** | almacena: carácter Unicode  <br>

**boolean** | almacena: evariable booleana| rango: False - True <br>

Los PRIMITIVOS DE TIPO ENTEROS son: byte, short, int, long. <br>

Los PRIMITIVOS FLOTANTES son: float y double. Se recomienda utilizar double porque tiene más decimales significativos, es más exacto. <br>

Un char representa CARACTERES INDIVIDUALES y contiene más de 30.000 caracteres codificaos distintos (lo que cubre los idiomas escritos más importantes), el subconjunto es el ASCII. <br>


## CONSTANTES

Las constantes enteras pueden represetnarse en notación decimal, octal (prefijo 0) o hexadecimal (prefijo ox o OX). <br>

Una **constante de caracteres** se encierra entre una pareja de **comillas simples**, como por ejemplo 'a'.<br>
una **constante de cadena** se encierra entre una pareja de **comillas dobles**, como por ejemplo "hola". <br>

Existen las **secuencias de escape** que tiene usos específicos, por ejemplo: <br>
   * \n new line (nueva linea)
   * \' comilla simple
   * \" comilla doble
   
## DECLARACION E INICIALIZACION DE TIPOS PRIMITIVOS

Se declaran proporcionando: **tipo**, **nombre (identificador)** y opcionalmente su **valor inicial** (cuando las declaro e inicializo al mismo tiempo). <br>

El **identificador** puede tener letras, numeros y caracteres de guión bajo, peor no puede empezar por un díigito. Tampoco pueden utilizar palabras reservadas. <br>
java es **case sensitive** hay que ver con detalle mayúsculas y minúsculas. <br>
Se nombran mediante **camelCase** . <br>

La colocación de una declaración determina su ámbito y su significado. <br>

Ejemplos:

```
int num3;    //inicialización predetermianda
double minimunWage = 4.50;       /7inicializacion standard
int x = 0, num1 = 0;  //se declaran dos entidades
int mun2 = num1;
```

---


## ENTRADA Y SALIDA POR TERMINAL

**nextLine** y **println**. <br>
Flujo de entrada **System.in** y flujo de calida **System.out** . <br>
Para leer **String** asociamos un objeto **Scanner** con **system**. <br>

---

## OPERADORES BÁSICOS

OPERADOR DE ASIGNACIÓN : <br>
   * = 
   * +=  suma el valor situado en el lado derecho (del propio operador) a la variable indicada del lado izquierdo, por ejemplo : x+=1 es lo mismo que x = x + 1.
   * -=  resta  el valor situado en el lado derecho (del propio operador) a la variable indicada del lado izquierdo, por ejemplo : x-=1 es lo mismo que x = x - 1.
   * *=  multiplica  el valor situado en el lado derecho (del propio operador) a la variable indicada del lado izquierdo, por ejemplo : X*=2 es lo mismo que X = X x 2.
   *  /=  divide  el valor situado en el lado derecho (del propio operador) a la variable indicada del lado izquierdo, por ejemplo : X/=3 es lo mismo que X = X / 3.
   
   
## OPERADORES ARITMÉTICOS BINARIOS

   * +SUMA
   * -RESTA
   * *MULTIPLICACION
   * /DIVISION
   * %MODULO (el residuo de la division, el resto)


## OPERADORES UNARIOS

   * -MENOS UNARIO, niega
   
   * ++AUTOINCREMENTO, que suma 1 a una variable. INCREMENTO PREFIJO (++X el valor de la expresión será el nuevo valor de X) o INCREMENTO POSTFIJO (X++ el valor de la expresión es el valor original).
   
   * --DECREMENTO, que resta 1 a una variable


## CONVERSIONES DE TIPO 

El **operador de conversión de tipo** se utiliza para generar una entidad temporal de un tipo. Por ejemplo:

```
int x = 6;
int y = 10;
quotient = (double) x / y;  
```
Como el resultado es un número flotante, debo convertirlo de integer a float. <br>


---

## INTRODUCCION CONDICIONALES


### OPERADORES RELACIONALES Y DE IGUALDAD

Los **operadores de igualdad** son: 
   * == (son iguales)
   * != (no son iguales)

Los **operadores relacionales** son: <br>

```
>    // mayor que 
>=   // mayor o igual que
<    // menor que 
<=   // menor o igual que 
```

Los operadores relacionales tienen una precedencia inferior a los operadores aritméticos, pero mayor precedencia que lso operadores de asignación, de modo que frecuentemente es innecesario utilizar paréntesis. <br>
Todos estos operadores se asocian de izquierda a derecha.

### OPERADORES LÓGICOS

   *  &&  ( AND ) - conjunción -
   *  ||  ( OR) - disyunción -
   *  !  ( NOT ) - negación - 
   
&& y || son operaciones de **evalucación cortocircuitables** , si el resultado puede determinarse examinando la primer expresión, entonces no se evalúa la segunda expresión. Por ejemplo: x != 0  &&  1/x 1= 3 . <br>
Si X es 0, la primer mitad es false y entonces el resultado de && es false, no calculo la segunda expresión. <br>

---


### IF

Su estructura es: <br>
if ( expresion )
  instruccion  <br>
siguiente instruccion  <br>

Si la expresión se evalúa como True, entonces se ejecuta instrucción, en caso contrario, no se ejecuta.  <br>
Cuando se completa la instrucción if el control pasa a la siguiente instrucción.  <br>


## IF ELSE

Su estructura es:  <br>

if ( expresion )  <br>
  instruccion1  <br>
else  <br>
  instruccion2  <br>
siguiente instruccion  <br>

Si la expresión se evalúa como True, se ejecuta la instruccion1, sino se ejecuta la isntruccion2.  <br>
Y luego pasa el control a la próxima instrucción.  <br>

Ejemplo:  <br>

```
if( x == 0) {
  System.out.println( "x is zero" );
} else {
  System.out.println( "x is : " );
  System.out.println( x );
}
```

Las instrucciones if pueden ser a su vez incluida dentro de una cláusala **if** o **else**, al igual que otras instrucciones de cotrol. <br>

 
## WHILE

Un ejemplo: <br>

while( expresion ) <br>
  instruccion <br>
siguiente instruccion <br>  

Si la expresión inicial es False, entonces nunca se ejecutará. <br>
Mientras que la espreción es True, se ejecuta al instrucción. <br>
Para evitar el bucle infinito, hay que ver que la condición en algún momento pase a ser False. <br>

## FOR


Para las iteraciones simples.<br>
Por ejemplo: <br>

for( inicializacion; comprobacion; actualizacion ) { <br>
  instruccion <br>
} <br>

La instrucción for se ejecuta realizando primero la incialización, después que se comprueba que es true, se lleva a cabo las dos acciones sigueintes: se ejecuta la instrucción y luego se realiza la actualización. <br>

Ejemplo: <br>

```
for( int i = 1; i <= 100; i++) {
  System.out.println( i);
}
```

Los bucles también puede anidarse, por ejemplo : <br>

```
for( int i = 1; i <= 10; i ++) {
  for(int j = 1; j <= 10; j ++) {
    if(i+j == i*j) {
      System.out.println( i + "." + j);
    }
  }
}
```
 
## DO

La comprobación se realiza después de haber ejecutado la instrucción especificada, siempre se ejecuta, al menos una vez. <br>

Ejemplo de sistaxis: <br>

do { <br>
  Pedir datos al usaurio; <br>
  Leer el valor; <br>
} while (el valor no sea correcto); <br>  
  

## BREAK Y CONTINUE

**BREAK** puede estar dentro de un if y también se encuentra en un switch. <br>
Dentro de un  if lo que hace es salir y pasar al próximo bloque de código. <br>
Break hace que se salga del bucle o instrucción switch más internos. <br>
La instrucción break etiquetada permite salir de un bucle anidado.<br>

**CONTINUE** termina la iteracción actual de un bucle y se pasa directamente a la siguiente iteración. <br>
Incluye ; y se utiliza en un bucle interno. <br>


## SWITCH

Se utiliza para seleccionar entre varios valores pequeños de tipo entero (o caracter). <br>
Está compuesta por uan expresión y un bloque. <br>
El bloque contiene una secuencia de instrucciones y una colección de etiquetas. <br>
luego de cada case tengo el break y al final puedo tener un caso default. <br>


## OPERADOR CONDICIONAL

Es una abreviatura para instrucciones if-else simples. <br>
Su formato es: <br>

**comprobacionExp ? exprSi : exprNo** <br>

En primer lugar se evalúa comprobacionExpr, seguida por exprSi o exprNo, generando así el resultado de la expresión completa. <br>
exprSi se evalúa si la comprobacionExp es True. <br>
En caso contrario se evalua exprNo.<br>

  
---

## MÉTODOS

Es lo que se llama **función** o **procedimiento** en otros lenguajes. <br>
Una **cabecera del método** consta de un **nombre**, una **lista de parámetros** (posiblemente vacia) y un tipo de **retorno**. <br>
El **cuerpo del método** es el código concreto para implementar el método, es un **bloque**. <br>
Una declaración de método consta de una cabecera y un cuerpo. <br>

Ejemplo: <br>

```
public class MinTest {

  public static void main(String [] args) {
  
    int a = 3;
    int b = 7;
    System.out.println(min(a,b));
  }
  //declaración del método
  public static int min( int x, int y) {
    return x < y ? x : y;
  }
  
}
```

El nombre del método es un **identificador**. <br>
La lista de parámetros está compuesta por cero o más parámetros formales, cada uno de ellos con un tipo especificado. <br>
Cuando se invoca un método, los argumentos reales se envían a los parámetros formales usando la asignación normal. <br>
Los tipos primitivos se pasan utilizando únicamente paso de parámetros de tipo paso por valor. <br>
Los argumentos reales no pueden ser modificados por la función. <br>
La instrucción return se utiliza para devolver un valor al llamarte. <br>
Si el tipo de retorno es **void**, entonces no se devuelve valor y no se debe utilizarse return dentro del método. <br>


## NOMBRES DE MÉTODOS SOBRECARGADOS

Java permite la sobrecarga de los nombres de métodos. Esto significa que **puede haber varios métodos con el mismo nombre** y que **tods ellos pueden declararse con el mismo ámbito de clase**, siempre y cuando sus **signaturas** (los tipos de su lista de parámetros) sean distintas. <br>
Puede haber dos signaturas que tengan el mismo número de parámetros, siempre y cuando al menos uno de los tipos de esos parámetros sea distinto. <br>
El tipo de retorno no se incluye en la signatura. No se puede tener dos métodos con el mismo ámbito de clase que solo se diferencien por el tipo de retorno.<br>
Los métodos con diferentes ámbitos de clase pueden tener los mismos nombres, las mismas signaturas e incluso los mismos tipos de retorno. <br>

## CLASES DE ALMACENAMIENTO

Las entidades (variables) que e declaran dentro del cuerpo de un método son **varaibles locales** y solo se pueden acceder a ellas por su nombre dentro del cuerpo del método. Esta entidades se crean al ejecutarse el cuerpo del método y desaparecen cuando el cuerpo del método termina. <br>

Una varaible decalrada fuera del ceurpo de un método será **global** para esa clase. Si se utiliza tanto **static** como **final** serán constantes simbólicas globales. <br>

Por ejemplo: <br>

```
static final double PI = 3.1415926535897932;
```

las constantes se escriben todo en mayúscula.  Si tiene más de uan palabra se separa con guión bajo ( _ ).<br>


---


# RESUMEN

**BLOQUE** es una secuencia de instrucciones enceradas entre llaves. <br>

**BREAK** es una instrucción que permite salir de bloque o switch más interno. <br>

**BREAK ETIQUETADA ( INSTRUCCIÓN)** es utilizada para salir de bucles anidados. <br>

**CABECERA DE MÉTODO** está compuesta por el nombre, el tipo de reorno y la lista de parámetros. <br>

**CONSTANTE DE CADENA** es una constante compuesta de caracteres encerrados entre dobles comillas. <br>

**CONTINUE** es una instrucción que hace que se salte a la sigueinte iteración del bucle más interno. <br>

**CODIGOS DE BYTES** es un código intermedio portable generado por el compilador Java.<br>

**COMENTARIOS** hacen que le código sea más fácil de leer por parte de las personas, pero no tienen ningún significado semántico. Java tiene 3 tipos de comentarios. <br>

**DECLARACIÓN DE MÉTODO** compuesta por CABECERA y CUERPO del MÉTODO.<br>

**DO** estructura de bucle qeu garantiza que el bucle se ejecute al menos una vez.<br>

**EVALUACIÓN CORTOCIRCUITABLE** si el resultado de un operador lógico puede determinarse examinando la primera expresión, entonces la segunda expresión no se evalúa. <br>

**FOR** es una estructura de bucl utilizada pricnipalmente para iteraciones simples. <br>

**IDENTIFICADOR** denomina una varaible o método. <br>

**IF** instrucción fundamental para la implementación de la toma de decisiones. <br>

**INSTRUCCIÓN NULA** compuesta por un solo punto y coma. <br>

**JAVA** su intérprete procesa código de bytes.<br>

**JAVAC** el compilador java, genera código de bytes. <br>

**MAIN** método especial que se invoca al ejecutarse el programa. <br>

**MÁQUINA VIRTUAL** el intérprete del código de bytes. <br>

**MÉTODO** el equivalente de java de función. <br>

**OPERADOR CONDICIONAL (?)** se utiliza en una expresión como abreviatura para instrucciones if-else sencillas. <br>

**OPERADOR DE CONVERSIÓN TIPO** para generar una varaible temporal sin nombre de un nuevo tipo. <br>

**OPERADORES ARITMÉTICOS BINARIOS** para efectuar las operaciones aritméticas básicas: +, -. *. / y %. <br>

**OPERADORES DE ASIGNACIÓN** para modificar el valor de una variable: =, +=, -=, *=, /=. <br>

**OPERADORES DE AUTOINCREMENTO (++) Y AUTODECREMENTO(--)** suman y restan 1, respectivamente. Hay dos formas: prefija y postfija. <br>

**OPERADORES DE IGUALDAD**: == y != para comparar valores, devuelven true o false. <br>

**OPERADORES LÓGICOS**: &&, || y !, simulan los conceptos de AND, OR, NOT. <br>

**OPERADORES RELACIONALES** <, <=, >, >=, devuelven true o false. <br>

**OPERADORES UNARIOS** requieren un operando: -, ++ o --. <br>

**PASO POR VALOR** el mecanismo de paso de parámetros en Java mediante el cual se copia el argumento real en el parámetro formal. <br>

**RETURN** devuelve la información al mmanate. <br>

**SECUENCIA DE ESCAPE** representa ciertas constantes de carácter. <br>

**SIGNATURA** nombre del método y de los tipos de lista de parámetros.

**SOBRECARGA DE NOMBRES DE MÉTODOS** permite que haya varios métodos con el mismo nombre, siempre y cuando los tipos de su  lista de parámetros difieran. <br>

**STATIC FINAL** constante global. <br>

**STATIC** es un método. <br>

**SWITCH** instrucción utilizada para seleccionar entre valores enteros peqeuños. <br>

**TIPO ENTEROS** byte, char, short, int y long. <br>

**TIPOS PRIMITIVOS** los enteros, de coma flotante, booleanos y de caracter. <br>

**UNICODE** conjunto internacinal de caracteres que contiene más de 30.000 cracteres (los lenguajes más importantes).<br>

**WHILE** la forma básica del bucle. <br>



---


## EJERCICIOS

   * ¿Cuáles son los ocho tipos primitivos de Java ?

   * Describe los tres tios de bucles existentes:  while, for y do.
   
   *  ¿Qué extensiones se utilizan para los archivos feuntes Java y para los archivos compilados?
   
   * ¿Qué es lo que hace la instrucción continue?
   
   * Describir el método de paso por valor.
   
   * Describir los tres tiòs de comentarios utilizados en programas Java.
   
   * ¿Qué es la sobrecarga de métodos?
   
   * ¿Cuál es la diferencia entre los operadores * y *=?
   
   * Describir todos los usos de una instrucción break. ¿Qué es uan instrucción break etiquetada?
   
   * Explicar la diferencia ebtre los operadores de incremento prefijo y postfijo.
