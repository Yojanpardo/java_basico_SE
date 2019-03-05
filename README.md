# Curso de Java básico SE de Platzi
En este repositorio se van a almacenar los archivos y notas tomadas durante el transcurso del curso.  
Encontramos java en muchísimos dispositivos, desde teléfonos celulares, controles remotos, hasta los servidores web que mueven el mundo tecnológico.

## Categorías de java
Existen java SE (Standar Edition) y EE (Entreprice Edition)

## Herramientas de desarrollo
para empezar debemos tener en nuestros computadores el JDK (Java Development Kit) y el JRE (Java Runtime Enviroment)

## Qué proyecto vamos a desarrollar?
Vamos a hacer una aplicación de consola que se va a llamar amazon viewer que nos va a ayudar a una cosa con las series lel.

## Qué es java?
Es un lenguaje de programación de alto nivel.  
__WORA__ Write Once Run Anywhere
* Simple
* Orientado a objetos
* Distribuido
* Arquitectura neutral
* Multi-hilo
* Portable
* Alto desempeño
* Seguro

## Origen de Java 
Nace en 1991 por James Gosling, fue adquirida por Sun Microsystems. Nació con la iniciativa de que un software fuera altamente portable y compatible.  
En 2009 Oracle adquiere Java y se genera una explosión de java.  
Existen dos categorías de Java que son la Standar Edition y java Enterprice edition. Existió una que se llamó java Micro Edition que era para dispositivos móviles.  
En este curso veremos todo lo que es java SE, su base y sintaxis para el desarrollo de aplicaciones web y móviles.  

## Herramientas de desarrollo
Necesitamos dos componentes importantes que son el JDK y el JRE para desarrollar y ejecutar nuestros programas.  
Yo estoy utilizando Ubuntu 18.04 y voy a mostrar los comandos necesarios para instalar java en este sistema operativo.

### Instalando java en Ubuntu 18.04
Debemos actualizar nuestros repositorios, instalar el JRE y el JDK más recientes.
~~~sh
$ sudo apt update
$ sudo apt install default-jre
$ sudo apt install default-jdk
~~~
Y listo tendremos java instalado en nuestro Ubuntu, si queremos verificarlo ejecutamos los siguientes comandos:
~~~sh
$ java --version
$ javac 
~~~
Si la salida al ejecutar estos comandos es algo como un error pues entonces está mal instalado o no lo está, así que regresa al paso anterior e intentalo nuevamente.

## Java Virtual Machine 
Java es ejecutado en una máquina virtual y por esto es tan portable, lo que hace es que tenemos nuestro código de java, java genera un código llamado Byte Code y este es traducido al lenguaje de la máquina para poder ser ejecutado.

## Definiendo la versión de java 
Cuando estamos trabajando en diferentes proyectos a veces nos encontramos con que utilizamos diferentes versiones de java, por ejemplo en mi universidad con fines de aprendizaje utilizamos las versiones más recientes de java y para proyectos laborales se ve necesario utilizar la versión 1.6, entonces en Ubuntu puedo cambiar la versión de java que necesite en cualquier momento con el siguiente comando.
~~~sh
$ sudo update-alternatives --config java
There are 2 choices for the alternative java (providing /usr/bin/java).

  Selection    Path                                            Priority   Status
------------------------------------------------------------
* 0            /usr/lib/jvm/java-11-openjdk-amd64/bin/java      1101      auto mode
  1            /usr/lib/jvm/java-11-openjdk-amd64/bin/java      1101      manual mode
  2            /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java   1081      manual mode

Press <enter> to keep the current choice[*], or type selection number: 2
update-alternatives: using /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java to provide /usr/bin/java (java) in manual mode
$ java -version                               
openjdk version "1.8.0_191"
OpenJDK Runtime Environment (build 1.8.0_191-8u191-b12-2ubuntu0.18.04.1-b12)
OpenJDK 64-Bit Server VM (build 25.191-b12, mixed mode)
~~~
Ese es todo el dialogo que aparece cuando quiero cambiar la version de java que necesito utilizar.

## Tipos de datos en Java
Existen los tipos de datos primitivo y tipo objeto

### Primitivos
Son los tipos de datos que se manejan por defecto dentro del lenguaje de Java y son los siguientes:

#### Numéricos enteros
Son los números enteros.

* byte
Ocupa un byte de memoria y puede contener valores entre -128 hasta 127
* short
Ocupa 2 bytes de memoria y puede contener valores entre -32.768 hasta 32.767
* int
Ocupa 4 bytes de memoria y puede contener valores entre -2.147.483.648 hasta 2.147.483.647
* long
Ocupa 8 bytes de memoria y puede contener valores entre -9.223.372.036.854.775.808 hasta 9.223.372.036.854.775.807
* Se declaran de la siguiente manera:
~~~java
byte age = 22
short born_year = 1996
int code = 161214217
long facebook_id = 899807866492738478L;
~~~

#### Punto flotante
Son números decimales.

* float
Ocupa 4 bytes de memoria y puede contener números decimales entre 
* double
Ocupa 8 bytes de memoria y puede contener números decimales entre 
* Se declaran de la siguiente manera
~~~java
float diametro = 34.25F;
double price = 5467.24321235654324343;
~~~

#### De texto
Almacenan caracteres y pueden ser:

* char
ocupa 2 bytes y tiene un rango unicode
* Se declaran de la siguiente manera
~~~java
char gender = 'M';
~~~

#### Lógicos
Son tipos de datos que son lógicos para hacer tareas lógicas 

* boolean
Es un tipo de datos que ocupa 2 bytes y tiene unicamente dos valores que son true o false
* Se declara de la siguiente manera
~~~java
boolean is_visible = true;
boolean works = false;
~~~

## Sintaxis
Java diferencia entre las mayúsculas, las variables deben iniciar solo con letras, '$' o '_', no pueden iniciar con nada más.  
Las constantes inician con mayúsculas y se separan con guiones bajos.  
las clases las vamos a declarar como Upper camel case y las variables y métodos se manejarán con lower camel case.

## Cast
Se trata de convertir una tipo de dato a otro tipo de dato.
Un casteo es automático cuando el espacio de memoria de la variable a castear es menor al de la nueva variable. de lo contrario hace falta un casta, de igual manera cuando se va a cambiar de un tipo de dato entero a un flotante o carácter. excepto de char a int.  
~~~java
short a = 100;
byte b = (byte) a;
~~~

## Arreglos
Los arreglos son objetos en los que podemos guardar mas de una variable, son como cajitas en las que podemos guardar muchas cosas y pueden ser de n dimensiones, entre mas complejo sea un arreglo, mas variables podrán almacenarse en él y se podrán acceder a ellos utilizando el indice de cada cajita.
~~~java
//aquí vamos a crear un par de arreglos de enteros
int[] codes; 
short años[];
//Definir el tamaño de los arreglos
variableName = new dataTipe[capacity];
//esta es otra forma de definir arreglo:
char[][] names = {
    {'y','o','j','a','n'},
    {'p','a','r','d','o'}
}//este es un arreglo dinámico 
~~~

### Búsqueda de elementos en arreglos
Para acceder a los elementos de un arreglo lo vamos a hacer por los indices, por ejemplo, si quiero acceder a la 'r' del arreglo creado anteriormente debería ingresar los indices de las cajas y si están anidadas unas dentro de otras pues cogiendo cada cajita y cuando llego a los elementos pues el indice del elemento, lo veremos a continuación.
~~~java
System.out.println(names[1][2]);
~~~
También se puede asignar un valor a un campo del arreglo con el indice
~~~java
names[0][0]='Y'
~~~

## Tipos de operadores en java

### Operadores aritméticos
|Símbolo|Nombre|Descripción|Aplicación|
|:-------:|------|-----------|:----------:|
|+|Suma|suma variables|c = a + b|
|-|Resta|resta variables|c = a - b|
|*|Multiplicación|multiplica variables|c = a * b|
|/|División|divide variables|c = a / b|
|%|Módulo|es el residuo de una división|c = a % b|  

### Operadores de asignación
Son operadores que nos ayudan a asignar valores a las variables.  

|Operador|Aplicación|Desglose|
|:--------:|:----------:|:--------:|
|+=|a += b|a = a + b|
|+=|a -= b|a = a - b|
|+=|a *= b|a = a * b|
|+=|a /= b|a = a / b|

### Operadores de incremento y decremento
|Operador|Nombre|Ejemplo|Desglose|
|:--:|:--:|:--:|:--:|
|++|Incremento|i++|i = i+1|
|--|Decremento|i--|i = i-1|

Se pueden escribir de dos maneras

|Prefijo|Posfijo|
|:--:|:--:|
|++i|i++|

### Operadores de equidad
Sirve para ver si dos datos son iguales o diferentes entre si y arroja datos booleanos.

|Operador|Nombre|Ejemplo|
|:-:|-|:-:|
|==|Igual|a == b|
|!=|Diferente|a != b|

### Operadores relacionales
|Operador|Nombre|Ejemplo|
|:-:|:-:|:-:|
|>|Mayor que|a > b|
|<|Menor que|a < b|
|>=|Mayor o igual que|a >= b|
|<=|Menor o igual que|a <= b|

Nos sirven para hacer comparaciones y nos regresa un valor booleano

### Operadores lógicos
|Operador|Nombre|Ejemplo|
|:------:|:----:|:-----:|
|   &&   |  and | a && b|
|  \|\|  |  or  | a || b|
|    !   |  not |   !a  |

Se utilizan con variables booleanas y sirven para ser utilizados en las tomas de decisiones.    

## Control de flujo 
para que nuestros programas funciones por lo general hay que tener un control sobre lo que está sucediendo y para ello podemos hacer uso de las condicionales con la ayuda de unas herramientas otorgadas por java que son los if, else, switch y bucles como while, do while, for, for each.  
Las condicionales utilizan operadores relacionales y lógicos para determinar el flujo de la información.  

### if else
Es la condicional básica, cuando la instrucción es cierta ejecuta una cosa y si no ṕues hace otra cosa. Se declaran de la siguiente manera:
~~~java
byte a = 1;
byte b = 2;

if (a < b){
  System.out.print('Si es menor');  
}else if (a==b){
    System.out.print('Son iguales');
}else{
    System.out.print('Ninguna de las dos')
}
~~~

### switch
Es similar al if else pero tiene mas caminos a escoger y se declara de la siguiente manera:
~~~java
switch(a){
    case valor1:
        System.out.print('aquí van unas acciones');
    break;
    case valor2:
        System.out.print('aquí van otras acciones');
    break;
    default:
        System.out.print('aqui van las acciones por default');
    break;
}
~~~
### Bucles
Son controles de flujo que se repetirán la cantidad de veces que lo deseemos.

#### While, do while, for, for each
~~~java
byte a = 10, b = 0;
while (a >= b){
    System.out.print(b);
    b++; 
}
//Se ejecutará 11 veces este ciclo

do{
    System.out.print(b);
    b++;
}while (a >= b);
//Se ejecutará al menos una vez

for (b=0; a>=b; b++ ) {
    System.out.println(b);
}
//Igual que el while pero con una linea menos

for (dataType variableName: array) {
    System.out.println(variableName);
}
~~~

Podemos recorrer un arreglo para leerlo o para rellenarlo utilizando un bucle, se recomienda más que todo hacer uso de un for o un foreach
~~~java
short[] array1=new short[5];
//Rellenando un array con un for
for (int i = 0; i < 5; i++) {
    array1[i] = i + 1;
    System.out.println("numero en la pocisión["+ i +"] = " + array1[i]);
}
//El foreach es más aspero porque si lel
for (short j : array1 ) {
    System.out.println(j);
}
~~~
