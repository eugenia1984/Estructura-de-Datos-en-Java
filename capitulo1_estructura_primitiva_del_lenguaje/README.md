# CAPITULO 1 : ESTRUCTURA PRIMITIVA DEL LENGUAJE

## El código fuente actualizado dle libro se puede ver en: http://www.cs.fiu.edu/vweiss

## Para consultas del libro: www.aw.com/csssupport

El código fuente Java reside en archivos cuyos nombres terminan con el sufijo **.java** .<br>
El compilador local, **javac**, compila y genera archivos **.class**, que contienen código de bytes. <br>
El **código de bytes Java** represetna el lenguaje intermedio portable que luego será interpretado ejecutando el **intérprete de Java**. <br>
El intérprete de Java se conoce con el nombre de **Máquina virtual**.<br>

## PRIMER PROGRAMA

```
public class FirstPrograma {
  
   public static void main( String [] args) {
   
    System.out.println("Is there anybody out there?" );
   }
}
```

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


## MAIN

Un programa Java está compuesto por una colección de **clases** que interactúan, las cuales contienen una serie de **métodos**. <br<
El equivalente de Java de las funciones y procedimientos es el **método estático**. <br>
Al ejecutar cualquier programa se invoca el método estático **main**. <br>

## SALIDAS A TRAVES DE TERMINAL

**println** es el mecanismo de salida principal en Java.

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
   
## DECALRACION E INCIIALIZACION DE TIPOS PRIMITIVOS

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

## ENTRADA Y SALIDA POR TERMINAL

**nextLine** y **println**. <br>
Flujo de entrada **System.in** y flujo de calida **System.out** . <br>
Para leer **String** asociamos un objeto **Scanner** con **system**. <br>

## OPERADORES BÁSICOS

OPERADOR DE ASIGNACIÓN : <br>
   * = 
   * +=  suma el valor situado en el lado derecho (del propio operador) a la variable indicada del lado izquierdo, por ejemplo : x+=1 es lo mismo que x = x + 1.
   * -=  resta  el valor situado en el lado derecho (del propio operador) a la variable indicada del lado izquierdo, por ejemplo : x-=1 es lo mismo que x = x - 1.
   * *=  multiplica  el valor situado en el lado derecho (del propio operador) a la variable indicada del lado izquierdo, por ejemplo : X*=2 es lo mismo que X = X x 2.
   *  /=  divide  el valor situado en el lado derecho (del propio operador) a la variable indicada del lado izquierdo, por ejemplo : X/=3 es lo mismo que X = X / 3.
   
## OPERADORES ARITMÉTICOS BINARIOS

   * +  SUMA
   * -  RESTA
   * *  MULTIPLICACION
   * /  DIVISION
   * %  MODULO (el residuo de la division, el resto)

## OPERADORES UNARIOS

   * - MENOS UNARIO, niega
   
   * ++ AUTOINCREMENTO, que suma 1 a una variable. INCREMENTO PREFIJO (++X el valor de la expresión será el nuevo valor de X) o INCREMENTO POSTFIJO (X++ el valor de la expresión es el valor original).
   
   * -- DECREMENTO, que resta 1 a una variable

## CONVERSIONES DE TIPO 

El **operador de conversión de tipo** se utiliza para generar una entidad temporal de un tipo. Por ejemplo:

```
int x = 6;
int y = 10;
quotient = (double) x / y;  
```
Como el resultado es un número flotante, debo convertirlo de integer a float. <br>


---

## INTORDUCCION CONDICIONALES


### OPERADORES RELACIONALES Y DE IGUALDAD

Los **operadores de igualdad** son: 
   * == (son iguales)
   * != (no son iguales)

Los **operadores relacionales** son:
   * >  (mayor que)
   * >=  (mayor o igual que)
   * <  (menor que)
   * <=  (menor o igual que)

Los operadores relacionales tienen una precedencia inferior a los operadores aritméticos, pero mayor precedencia que lso operadores de asignación, de modo que frecuentemente es innecesario utilizar paréntesis. <br>
Todos estos operadores se asocian de izquierda a derecha.

### OPERADORES LÓGICOS

   *  &&  ( AND ) - conjunción -
   *  ||  ( OR) - disyunción -
   *  !  ( NOT ) - negación - 
   
&& y || son operaciones de **evalucaciñon cortocircuitables** , si el resultado puede determinarse examinando la primer expresión, entonces no se evalúa la segunda expresión. Por ejemplo: x != 0  &&  1/x 1= 3 . <br>
Si X es 0, la primer mitad es false y entonces el resultado de && es false, no calculo la segunda expresión. <br>


   
