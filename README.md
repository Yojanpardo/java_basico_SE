# Curso de Java básico SE de Platzi
En seste repositorio se van a almacenar los archivos y notas tomadas durante el transcurso del curso.
Encontramos java en muchísimos dispositivos, desde telefonos celulares, controles remotos, hasta los serviders web que mueven el mundo tecnologico.

## Categorias de java
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
* Multihilo
* Portable
* Alto desempeño
* Seguro

## Origen de Java 
Nace en 1991 por James Gosling, fue adquirida por Sun Microsystems. Nació con la iniciativa de que un software fuera altamente portable y compatible.  
En 2009 Oracle adquiere Java y se genera una explosión de java.  
Existen dos categorías de Java que son la Standar Edition y java Enterprice edition. Existión una que se llamó java Microedition que era para dispositivos móviles.  
En este curso veremos todo lo que es java SE, su base y sintaxis para el desarrollo de aplicaciones web y móviles.  

## Heraamientas de desarrollo
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
Si la salida al ejecutar estos comandos es algo como un error pues entonces está mal instalado o no lo está, asi que regresa al paso anterior e intalalo nuevamente.

## Java Virtual Machine 
Java es ejecutado en una máquina virtual y por esto es tan portable, lo que hace es que tenemos nuestro código de java, java genera un codigo llamado Byte Code y este es traducido al lenguaje de la máquina para poder ser ejecutado.

## Definiendo la versión de java 
Cuando estamos trabajando en diferentes proyectos a veces nos encontramos con que utilizamos diferentes versiones de java, por ejemplo en mi universidad con fines de aprendizaje tulizamos las versiones más recientes de java y para proyectos laborales se ve necesario utilizar la versión 1.6, entonces en ubuntu puedo cambiar la versión de java que necesite en cualquier momento con el siguiente comando.
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
