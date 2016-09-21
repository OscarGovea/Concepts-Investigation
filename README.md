1. Patrón de diseño
----------
#### ¿Qué es un patrón de diseño?
*"Los patrones de diseño son el esqueleto de las soluciones a problemas comunes en el desarrollo de software.”*

Brindan una solución ya probada y documentada a problemas de desarrollo de software que están sujetos a contextos similares. Debemos tener presente los siguientes elementos de un patrón: su nombre, el problema (cuando aplicar un patrón), la solución (descripción abstracta del problema) y las consecuencias (costos y beneficios).

Existen varios patrones de diseño popularmente conocidos, los cuales se clasifican como se muestra a continuación:
> - **Patrones Creacionales:** Inicialización y configuración de objetos.
> - **Patrones Estructurales:** Separan la interfaz de la implementación. Se ocupan de cómo las clases y objetos se agrupan, para formar estructuras más grandes.
> - **Patrones de Comportamiento:** Más que describir objetos o clases, describen la comunicación entre ellos.

Para que una solución sea considerada un patrón debe poseer ciertas características:

> - Efectividad
> - Ser reutilizable

2. Patrón Singleton
----------
#### ¿En que consiste un patrón singleton?
Restringe la instanciación de una clase o valor de un tipo a un solo objeto.
Ejemplo:
```
public sealed class Singleton 
      { 
            private static volatile Singleton instance; 
            private static object syncRoot = new Object(); 
            private Singleton() 
            { 
                  System.Windows.Forms.MessageBox.Show("Nuevo Singleton"); 
            } 
            public static Singleton GetInstance 
            { 
                  get 
                  { 
                        if (instance == null) 
                        { 
                             lock(syncRoot) 
                             { 
                                   if (instance == null) 
                                         instance = new Singleton(); 
                             } 
                        } 
                        return instance; 
                  } 
            }
       }
```

3. Patrón Factory
----------
#### ¿En que consiste un patrón Factory?
Parte del principio de que las subclases determinan la clase a implementar.
```
public class ConcreteCreator extends Creator
  {
  protected Product FactoryMethod()
      {
            return new ConcreteProduct();
      }
}
public interface Product{}
public class ConcreteProduct implements Product{}
      public class Client
      {
            public static void main(String args[])
            {
                  Creator UnCreator;
                  UnCreator = new ConcreteCreator();
                  UnCreator.AnOperations();
            }
      }
```

4. Patrón Builder
----------
#### ¿En que consiste el patrón Builder? 
Es usado para permitir la creación de una variedad de objetos complejos desde un objeto fuente (Producto), el objeto fuente se compone de una variedad de partes que contribuyen individualmente a la creación de cada objeto complejo a través de un conjunto de llamadas a interfaces comunes de la clase Abstract Builder.

5. ADB de Android
--------------
#### ¿Qué es ADB? 
Las siglas ADB significan Android Debug Bridge y se corresponden con una herramienta de software que nos permite interactuar con nuestro smartphone Android desde un ordenador. Así, por ejemplo, a través de ADB podemos ejecutar comandos para copiar archivos desde el ordenador al teléfono o viceversa, flashear un revocery o el firmware completo e incluso reiniciar el dispositivo en modo recovery. 

Básicamente, en el ADB es la manera de cambiar profundamente el software de nuestro smartphone o por lo menos acceder a él. Por supuesto, todo esto se hace posible a través de un cable USB con el que conectamos el smartphone al ordenador.

> ***Nota:*** Para que nuestro ordenador reconozca el dispositivo necesitamos activar en el terminal la **depuración por USB**. En Ajustes > Información del teléfono pulsaremos varias veces sobre 'Número de compilación' hasta que aparezcan las opciones de desarrollo. Ahora entraremos en estas opciones y activaremos la 'Depuración por USB'. La primera vez que conectamos el teléfono al ordenador no preguntará si confiamos en el mismo.

6. Operador **final** en JAVA
------------
#### ¿Para que sirve el operador final en JAVA?
*FINAL:* Indica que una variable, método o clase no se va a modificar, lo cuál puede ser útil para añadir más semántica, por cuestiones de rendimiento, y para detectar errores.

> - Si una variable se marca como final, no se podrá asignar un nuevo valor a la variable.
> - Si una clase se marca como final, no se podrá extender la clase.
> - Si es un método el que se declara como final, no se podrá sobreescribir.

> **Nota:** Algo muy a tener en cuenta a la hora de utilizar este modificador es que si es un objeto lo que hemos marcado como final, esto no nos impedirá modificar el objeto en sí, sino tan sólo usar el operador de asignación para cambiar la referencia.

7. Sobre Carga de Operadores 
------------------------------
#### ¿Que Lenguajes soportan Sobre Carga de operadores? 
La sobrecarga de operadores es uno de los mecanismos que nos permite ampliar las capacidades de los lenguajes de programación orientados a objetos. Algunos lenguajes que soportan ésta característica son:
> - C
> - C#
> - C++
> - Python
> - Java

8. Gradle 
----------
#### ¿Para que sirve Gradle? 
Gradle es una herramienta para automatizar la construcción de nuestros proyectos, por ejemplo las tareas de compilación, testing, empaquetado y el despliegue de los mismos. Es muy flexible para la configuración, pero además ya tiene armadas las tareas para las mayoría de los proyectos por default. 

Gradle es un sistema de compilación que reune en un uno solo las mejores prestaciones de otros sistemas de compilación. Está basado en JVM (Java Virtual Machine), lo que significa que puedes escribir tu propio script en java, y que Android Studio lo entenderá y lo usará.

Lo mejor de gradle es que es un plugin, lo que facilita su actualización y su exportación de un proyecto a otro. Esto significa que puedes tener tu propio lenguaje de programación  y automatizar el proceso de compilación en un solo paquete (de la misma manera que un jar en caso de java)  y poder distribuirlo al resto del mundo

#### ¿Por qué google ha creado Gradle?

Google ha creado uno de los sistemas de compilación más avanzados del mercado para permitir a todos los usuarios escribir sus propios scripts sin necesidad de aprender ningún nuevo lenguaje, disminuyendo asi la curva de aprendizaje y permitiendo llegar a un mayor público la programación en Android.

9. Injección de Dependencias en Desarrollo de Software
-----------
#### ¿En que consiste la injección de dependencias en desarrollo de software, y por qué es conveniente utilizarla?
La inyección de dependencias es un patrón de diseño de software usado en la Programación Orientada a Objetos, que trata de solucionar las necesidades de creación de los objetos de una manera práctica, útil, escalable y con una alta versatilidad del código.

En la mayoría de los frameworks actuales se aplica la Inyección de dependencias como parte de las herramientas y modelos que facilitan al programador. Como cualquier patrón de diseño de software trata de solucionar de una manera elegante un problema habitual en el desarrollo de software, por lo que también es idóneo utilizar este patrón en el desarrollo de proyectos a pequeña escala.

Este patrón, como muchos otros, nos ayuda a separar nuestro código por responsabilidades, siendo que en esta ocasión sólo se dedica a organizar el código que tiene que ver con la creación de los objetos.