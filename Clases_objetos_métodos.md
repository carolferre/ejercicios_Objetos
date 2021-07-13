# ejercicios_Objetos

POO EN PYTHON:
--------------

Clase: es un modelo donde se redactan las características comunes de un grupo de objetos.
Ejemplo de un coche la clase sería el chasis y las ruedas (características comunes de los coches).


class Coche():
  largoChasis=250
  
  anchoChasis=120
  
  ruedas=4
  
  enmarcha=False
 
 Nuesstra clase Coche tiene 4 propiedades.
 
 Comportamiento: un objeto tiene un comportamiento, este viene determinado por métodos.
 Ejemplo, un coche puede tener muchos comportamientos, como arrancar, acelerar, frenar, girar.
 
 Diferencia entre función y método: un método (defs) es un tipo de función especial que pertenece a la clase, mientras que una función (def nombreFuncion(self): no pertenece a ninguna clase.
 Esto es un ejemplo de método:
 
  def arrancar (self):
  
  pass
  
Self hace referencia al propio objeto perteneciente a la clase, o a la instancia perteneciente a la clase. Este self es exactamente igual que this en java, python nos obliga a ponerlo en todos los métodos pertenecientes a  las clases.
pass aparece porque la función está vacía, en cuanto esté llena se elimina el pass.


def arrancar(self):
  self.enmarcha=True
  
 Con este método dice que el coche está arrancado.

def estado(self):
  if(self.enmarcha):
    return "El coche está en marcha"
  else:
    return "El coche está parado"
    
  Es una comprobación que nos dice si el coche está en marcha o parado
  
  
Ejemplar/instancia y objeto de clase son sinónimos: es un ejemplar perteneciente a una clase.
Ejemplo tanto citroen como peugeot son coches que comparten unas características en común, los dos tienen 4 ruedas y tienen chasis (características comunes pertenecientes a la clase coche). También
puede que tengan características diferentes definidas dentro del propio objeto.

miCoche=Coche()
nombredelobjeto=nombredelaClase()

Hemos instanciado una clase o creado un objeto llamado miCoche

Modularización: Normalmente un programa de objetos está compuesto por varias clases. Cada uno de estos elementos o módulos funcionan de forma independiente.
Permite reutilizar trozos de código de un programa a otro. Si una de las clases fallan el resto del programa funcionará, no se cae por completo.

Encapsulación: el funcionamiento interno de esa clase está encapsulado del exterior, protegido, nada se sabe de él desde otra clase. Sin embargo todas las clases están conectadas para que funcionen como un equipo pero a la vez cada uno de las clases está encapsulada para que el funcionamiento interno n o sea accesible desde fuera.

Métodos de acceso: creándolas se consigue que las clases funcionen como un equipo.
Ejemplo el cd le pide al volumen que suba el sonido.

Nomenclatura del punto: se usa para acceder a las propiedades o comportamientos del objeto. Ejemplo miCoche.color="rojo";
miCoche.peso=1500;

print("El largo del coche es: ",miCoche.largoChasis)
Nos imprime 250

print("El coche tiene ",miCoche.ruedas," ruedas")
Nos dice que el coche tiene 4 ruedas

Para llamar al método sería: miCoche.arrancar()
El resultado será True ya que el coche está en marcha.


El programa entero sería:

class Coche():

  largoChases=250
  
  anchoChasis=120
  
  ruedas=4
  
  enmarcha=Flase
  
  
  def arrancar (self):
    
    self.enmarcha=True
    
    
  def estado(self):
  
    if (self.enmarcha):
    
      return "El coche está en marcha"
      
    else:
    
      return "El coche está parado"
  
miCoche=Coche()

print("El largo del coche es: ",miCoche.largoChasis)

print("El coche tiene ",miCoche.ruedas," ruedas")

miCoche.arrancar()

print(miCoche.estado())
