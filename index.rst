Tarea # 2 Allan Quesada Fuentes
=======================
.. figure:: ../C:\Users\Allan Quesada\Desktop\Progra 3\diagram.png
    :align: right
    :figwidth: 300px
    :target: ../C:\Users\Allan Quesada\Desktop\Progra 3\diagram.png

Manejo de Herencia en C#
=======================
Deficicion:
----------- 
La herencia es un tipo de jerarquia que nos permite reutilizar, y modificar nuevas clases apartir de otras ya existentes.
La clase cuyos miembros se heredan se denomina clase base y la clase que hereda esos miembros se denomina clase derivada.

Clases Abstractas
-----------------
Son las clases que solo se pueden utilizar como clase base en una relación de herencia.
es una que está diseñada sólo como clase padre de las cuales se deben derivar clases hijas. 
No es posible hacer una implementación de una clase abstracta pero de una clase derivada de esa clase abstarcta si.

Interfaces
-----------
Las interfaces describen un grupo de comportamientos relacionados que pueden pertenecer a cualquier clase o estructura. Las interfaces pueden estar compuestas de métodos, propiedades, eventos, indizadores o cualquier combinación de estos cuatro tipos de miembros

Ejemplo
-----------
La interface se define

    interface IEquatable<T>
    {
    bool Equals(T obj);
    }

Implementacion de una interface

    public class Car : IEquatable<Car>
    {
    public string Make {get; set;}
    public string Model { get; set; }
    public string Year { get; set; }

    // Implementation of IEquatable<T> interface
    public bool Equals(Car car)
    {
        return this.Make == car.Make &&
               this.Model == car.Model &&
               this.Year == car.Year;
    }
}

Manejo de Exepciones
====================
Exepciones 
-----------
Las excepciones las inicia el código que encuentra un error y las detecta el código que puede corregir dicho error. Las excepciones puede iniciarlas .NET Framework Common Language Runtime o el código de un programa.

Las excepciones están representadas por clases derivadas de Exception. Esta clase identifica el tipo de excepción y contiene propiedades que tienen los detalles sobre la excepción. Iniciar una excepción implica crear una instancia de una clase derivada de excepción, configurar opcionalmente las propiedades de la excepción y luego producir el objeto con la palabra clave throw.
 
Try:
----
Un bloque de prueba identifica un bloque de código para el cual se activan excepciones particulares. Es seguido por uno o más bloques de captura.

Catch:
------
Un programa detecta una excepción con un controlador de excepciones en el lugar de un programa en el que desea manejar el problema. La palabra clave catch indica la captura de una excepción.

Finally:
--------
El bloque finally se utiliza para ejecutar un conjunto dado de sentencias, ya sea que se lance una excepción o no. Por ejemplo, si abre un archivo, debe cerrarse si se produce una excepción o no.

Ejemplo:
--------

using System;

namespace ErrorHandlingApplication {
   class DivNumbers {
      int result;
      
      DivNumbers() {
         result = 0;
      }

      public void division(int num1, int num2) {
         try {
            result = num1 / num2;
         } catch (DivideByZeroException e) {
            Console.WriteLine("Exception caught: {0}", e);
         } finally {
            Console.WriteLine("Result: {0}", result);
         }
      }

      static void Main(string[] args) {
         DivNumbers d = new DivNumbers();
         d.division(25, 0);
         Console.ReadKey();
      }
   }
}



Referencias
------------------
* `Sam, S. (13 de 08 de 2018). TutorialsPoint. Obtenido de Try-Catch-Finally in C#:     https://www.tutorialspoint.com/Try-Catch-Finally-in-Chash`
* `DocsMicrosoft. (19 de 07 de 2015). Obtenido de Usar excepciones (Guía de programación de C#):    https://docs.microsoft.com/es-es/dotnet/csharp/programming-guide/exceptions/using-exceptions`
* `DocsMicrosoft. (20 de 08 de 2018). Obtenido de Interfaces: https://docs.microsoft.com/en-    us/dotnet/csharp/programming-guide/interfaces/`
* `Lopez, Y. (2007). Iniciacion en la Programacion C#. Obtenido de Un Enfoque Practico:     https://books.google.es/books?                  hl=es&lr=&id=RISjyT8ts7QC&oi=fnd&pg=PA1&dq=clases+abstractas+c%23&ots=dzD-45Jhv8&sig=AZsqPuGW_Sv6nXfn0CiMO4ouq3Q#v=onepage&q=clases%20abstractas%20c%23&f=false`



