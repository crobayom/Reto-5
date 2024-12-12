# Asuma que el pinguno es un cilindro
En este repositorio se socializara el recorrido para cumplir con el reto 5

##1. 


### 1) Calcular volumen y area superficial (matematica)

Volumen: 

(4/3)*pi*r1**3+pi*r2**2*h*(1/3)


Area:

4*pi*r1**2+pi*r2**2+pi*r2*((r2**2+h**2)**0.5)


### 2) Crear dos funciones para calcular el volumen y el area superficial

```
def volumen_figura (pi:float,r1:float,r2:float,h:float,volumen:float) -> float:
  volumen:float=(4/3)*pi*r1**3+pi*r2**2*h*(1/3)
  return volumen


def volumen_figura (pi:float,r1:float,r2:float,h:float,area:float) -> float:
  area:float=4*pi*r1**2+pi*r2**2+pi*r2*((r2**2+h**2)**0.5)
  return area
```

### 3) Como usar pi con  import math y math.pi

Luego de investigar encontre que para usar a pi con la biblioteca math, y definiendo una variable igualada a la operacion matematica definida math.pi
de esta manera:

```
import math
pi=math.pi
print(pi)
```

Ejecutando este codigo se podra ver el numero que se le asigno al identificador elegido, la longitud de este dependera de la presicion disponible

4) Finalmente el programa completo teniendo ambos calculos, seria el siguiente:

```
import math
pi=math.pi
def volumen_figura (pi:float,r1:float,r2:float,h:float,volumen:float) -> float:
  volumen:float=(4/3)*pi*r1**3+pi*r2**2*h*(1/3)
  return volumen

def volumen_figura (pi:float,r1:float,r2:float,h:float,area:float) -> float:
  area:float=4*pi*r1**2+pi*r2**2+pi*r2*((r2**2+h**2)**0.5)
  return area

if __name__=="__main__":
  pi:float
  r1:float
  r2:float
  h:float
  volumen:float
  
  volumen_figura()
  print(volumen)
```

2. a


Calcular area y perimetro (matematica):
Area: 
b*a+2*r**2*pi

Perimetro:
2b+2a+2*(2*pi*r)

def area_figura (b:float,a:float,r:float,pi:float) -> float:
  area:float
  area=b*a+2*r**2*pi
  return area

def perimetro_figura (b:float,a:float,r:float,pi:float) -> float:
  perimetro:float
  perimetro=2*b+2*a+2*(2*pi*r)
  return perimetro

#Como usar pi con  import math y math.pi

#Como usar pi con  import math y math.pi

Luego de investigar encontre que para usar a pi con la biblioteca math, y definiendo una variable igualada a la operacion matematica definida math.pi
de esta manera:

´´´
import math
pi=math.pi
print(pi)
´´´

Ejecutando este codigo se podra ver el numero que se le asigno al identificador elegido, la longitud de este dependera de la presicion disponible                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          

3. 

def kilos_animales (gallinas:int,gallos:int,pollitos:int,peso:int):
  gallinas:int
  gallos:int
  pollitos:int
  peso:int
  peso=gallinas*6+gallos*7+pollitos                          
  return peso

4. 
   
def promedio_numeros (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float,promedio:float) -> float:
  primero:float
  segundo:float
  tercero:float
  cuarto:float
  quinto:float
  promedio:float=(primero+segundo+tercero+cuarto+quinto)/5
  return promedio

def promedio_multiplicativo_numeros (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float,promedio:float) -> float:
  primero:float
  segundo:float
  tercero:float
  cuarto:float
  quinto:float
  promedio:float=(primero*segundo*tercero*cuarto*quinto)**(1/5)
  return promedio

def potencia_del_mayor_numero_elevado_al_menor_numero (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float,promedio:float) -> float:
  primero:float
  segundo:float
  tercero:float
  cuarto:float
  quinto:float
  promedio:float=(primero+segundo+tercero+cuarto+quinto)/5
  return promedio

def promedio_numeros (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float,promedio:float) -> float:
  primero:float
  segundo:float
  tercero:float
  cuarto:float
  quinto:float
  promedio:float=(primero+segundo+tercero+cuarto+quinto)/5
  return promedio


5. #Consultar qué es y cómo funciona pip en python.

6. #Hacer un listado de módulos populares para python que se puedan instalar com pip y consultar cómo instalarlos.




