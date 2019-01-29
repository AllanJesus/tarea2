Tarea # 2 Allan Quesada Fuentes
=======================

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
´´´C#
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
´´´

Manejo de Exepciones
====================
Exepciones 
-----------
Las excepciones las inicia el código que encuentra un error y las detecta el código que puede corregir dicho error. Las excepciones puede iniciarlas .NET Framework Common Language Runtime o el código de un programa.

Las excepciones están representadas por clases derivadas de Exception. Esta clase identifica el tipo de excepción y contiene propiedades que tienen los detalles sobre la excepción. Iniciar una excepción implica crear una instancia de una clase derivada de excepción, configurar opcionalmente las propiedades de la excepción y luego producir el objeto con la palabra clave throw.

class CustomException : Exception
       {
           public CustomException(string message)
           {
              
           }

       }
       private static void TestThrow()
       {
           CustomException ex =
               new CustomException("Custom exception in TestThrow()");

           throw ex;
       }



Referencias
------------------

* `Sphinx documentation`_
* `RestructuredText primer`_
* `An introduction to Sphinx and Read the Docs for technical writers`_
