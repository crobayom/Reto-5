# Asuma que el pinguno es un cilindro
En este repositorio se socializara el recorrido para cumplir con el reto 5

##1. 

[Ejercicio 1](https://camo.githubusercontent.com/9a79fe9629fff1ceecb5860dba4054b90da7acda3d4f2c9cd7f62a34799894d2/68747470733a2f2f692e706f7374696d672e63632f465276436d7078782f696d6167652e706e67)


### 1) Calcular volumen y area superficial (matematica)

Volumen: 

(4/3)*pi*r1**3+pi*r2**2*h*(1/3)


Area:

4*pi*r1**2+pi*r2**2+pi*r2*((r2**2+h**2)**0.5)


### 2) Crear dos funciones para calcular el volumen y el area superficial

```
def volumen_figura (PI:float,r1:float,r2:float,h:float) -> float:
  volumen=(4/3)*PI*r1**3+PI*r2**2*h*(1/3)
  return volumen


def area_figura (PI:float,r1:float,r2:float,h:float) -> float:
  area=4*PI*r1**2+PI*r2**2+PI*r2*((r2**2+h**2)**0.5)
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
PI=math.pi
def volumen_figura (PI:float,r1:float,r2:float,h:float) -> float:
  volumen=(4/3)*PI*r1**3+PI*r2**2*h*(1/3)
  return volumen

def area_figura (PI:float,r1:float,r2:float,h:float) -> float:
  area=4*PI*r1**2+PI*r2**2+PI*r2*((r2**2+h**2)**0.5)
  return area

if __name__=="__main__":
  r1:float
  r2:float
  h:float
  
  r1=float(input("Ingrese el valor del primer radio 'de la esfera': "))
  r2=float(input("Ingrese el valor del segundo radio 'del cono': "))
  h=float(input("Ingrese el valor de la altura 'del cono': ")) 

  
  print("El volumen total de la figura es: "+str(volumen_figura(PI,r1,r2,h)))
  print("El area superficial de la figura es: "+str(area_figura(PI,r1,r2,h)))
```

## 2. 

[Ejercicio 2](https://camo.githubusercontent.com/1e035694c4675debe6703e3771f67ff06d8da330997d02c3806aa2bd5936bc54/68747470733a2f2f692e706f7374696d672e63632f3174344d727a734c2f696d6167652e706e67)

### 1) Calcular area y perimetro (matematica):

Area: 
b*a+2*r**2*pi

Perimetro:
2b+2a+2*(2*pi*r)

### 2) Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r, a y b.


```
def area_figura (b:float,a:float,r:float,PI:float) -> float:
  area:float
  area=b*a+2*r**2*PI
  return area

def perimetro_figura (b:float,a:float,r:float,PI:float) -> float:
  perimetro:float
  perimetro=2*b+2*a+2*(2*PI*r)
  return perimetro
```

### 3) Como usar pi con  import math y math.pi

Luego de investigar encontre que para usar a pi con la biblioteca math, y definiendo una variable igualada a la operacion matematica definida math.pi
de esta manera:

```
import math
pi=math.pi
print(pi)
```

### 4) Finalmente el programa completo teniendo ambos calculos, seria el siguiente:                                                                                                                                                                         

```
import math
PI=math.pi
def area_figura (b:float,a:float,r:float,PI:float) -> float:
  area:float
  area=b*a+2*r**2*PI
  return area

def perimetro_figura (b:float,a:float,r:float,PI:float) -> float:
  perimetro:float
  perimetro=2*b+2*a+2*(2*PI*r)
  return perimetro

if __name__=="__main__":
  b:float=float(input("Ingrese el valore de la base del rectangulo: "))
  a:float=float(input("Ingrese el valor de la altura del rectangulo: "))
  r:float=float(input("Ingrese el valor del radio de ambos circulos: ")) 

  print("El area de la figura es: "+str(area_figura(b,a,r,PI)))
  print("El perimetro de la figura es: "+str(perimetro_figura(b,a,r,PI)))
```

## 3. Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente. 

```
def kilos_animales (gallinas:int,gallos:int,pollitos:int):
  gallinas:int
  gallos:int
  pollitos:int
  peso:int
  peso=gallinas*6+gallos*7+pollitos                          
  return peso

if __name__=="__main__":
  gallinas:int=int(input("Ingrese la cantidad de gallinas: "))
  gallos:int=int(input("Ingrese la cantidad de gallos: "))
  pollitos:int=int(input("Ingrese la cantidad de pollitos: "))
  print("El peso total de carne de avez es: "+str(kilos_animales(gallinas,gallos,pollitos)))
```

## 4. Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.

```
def interes_compuesto (monto:float,interes:float,tiempo:float)->float:
    return monto*(1+interes/100)**tiempo

if __name__=="__main__":
    monto:float=float(input("Ingrese el monto inicial sobre el cual se hara el interes: "))
    interes:float=float(input("Ingrese el porcentaje de interes que se le aplicara mensualmente al monto 'sin incluir el signo de porcentaje': "))
    tiempo:float=float(input("Ingrese los meses que el monto se le aplicara el interes compuesto: "))

    print("El monto al final del periodo de tiempo de "+str(tiempo)+" meses, teniendo un interes de "+str(interes)+"% es: "+str(interes_compuesto(monto,interes,tiempo)))
```


## 4. Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.

```

def interes_compuesto (c:float,i:float,n:int) -> int:
  monto_final:float=c*(1+(i/100))**n
  return monto_final
if __name__=="__main__":
  c:float=float(input("Ingrese el monto inicial del prestamo: "))
  i:float=float(input("Ingrese el interes (porcentual sin el signo de porciento) por mes del monto: "))   
  n:int=int(input("Ingrese la cantidad de meses del prestamo: "))
  print("El monto final del prestamo de "+str(c)+" a un interes mensual de "+str(i)+"% por "+str(n)+" meses, es: "+str(interes_compuesto(c,i,n)))
  
```

## 5. Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una: 

[] El promedio

[] El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)

[] La potencia del mayor número elevado al menor número

[] La raíz cúbica del menor número



```
def promedio_numeros (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float) -> float:
  return (primero+segundo+tercero+cuarto+quinto)/5
```

[X] El promedio

[] El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)

[] La potencia del mayor número elevado al menor número

[] La raíz cúbica del menor número


```
def promedio_multiplicativo_numeros (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float) -> float:
  return (primero*segundo*tercero*cuarto*quinto)**(1/5)
```

[X] El promedio

[X] El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)

[] La potencia del mayor número elevado al menor número

[] La raíz cúbica del menor número


```
def numero_mayor_elevado_numero_menor (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float,menor:float,mayor:float) -> float:
  menor:float=0
  mayor:float=0
  if primero<segundo and primero<tercero and primero<cuarto and primero<quinto:
    menor=primero
  elif segundo<primero and segundo<tercero and segundo<cuarto and segundo<quinto:
     menor=segundo
  elif tercero<primero and tercero<segundo and tercero<cuarto and tercero<quinto:
    menor=tercero
  elif cuarto<primero and cuarto<segundo and cuarto<tercero and cuarto<quinto:
    menor=cuarto
  else:
    menor=quinto

  if primero>segundo and primero>tercero and primero>cuarto and primero>quinto:
    mayor=primero
  elif segundo>primero and segundo>tercero and segundo>cuarto and segundo>quinto:
    mayor=segundo
  elif tercero>primero and tercero>segundo and tercero>cuarto and tercero>quinto:
    mayor=tercero
  elif cuarto>primero and cuarto>segundo and cuarto>tercero and cuarto>quinto:
    mayor=cuarto
  else:
    mayor=quinto
  return mayor**menor
```

[X] El promedio

[X] El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)

[X] La potencia del mayor número elevado al menor número

[] La raíz cúbica del menor número


```
def raiz_cubica_del_menor_numero (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float,menor:float) -> float:
  menor:float=0
  if primero<segundo and primero<tercero and primero<cuarto and primero<quinto:
    menor=primero
  elif segundo<primero and segundo<tercero and segundo<cuarto and segundo<quinto:
     menor=segundo
  elif tercero<primero and tercero<segundo and tercero<cuarto and tercero<quinto:
    menor=tercero
  elif cuarto<primero and cuarto<segundo and cuarto<tercero and cuarto<quinto:
    menor=cuarto
  else:
    menor=quinto
  return menor**(1/3)
```

[X] El promedio

[x] El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)

[X] La potencia del mayor número elevado al menor número

[X] La raíz cúbica del menor número

Esto agrupado en un solo codigo, se veria de esta manera:
```
def promedio_numeros (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float) -> float:
  return (primero+segundo+tercero+cuarto+quinto)/5
def promedio_multiplicativo_numeros (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float) -> float:
  return (primero*segundo*tercero*cuarto*quinto)**(1/5)
def numero_mayor_elevado_numero_menor (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float,menor:float,mayor:float) -> float:
  if primero<segundo and primero<tercero and primero<cuarto and primero<quinto:
    menor=primero
  elif segundo<primero and segundo<tercero and segundo<cuarto and segundo<quinto:
     menor=segundo
  elif tercero<primero and tercero<segundo and tercero<cuarto and tercero<quinto:
    menor=tercero
  elif cuarto<primero and cuarto<segundo and cuarto<tercero and cuarto<quinto:
    menor=cuarto
  else:
    menor=quinto

  if primero>segundo and primero>tercero and primero>cuarto and primero>quinto:
    mayor=primero
  elif segundo>primero and segundo>tercero and segundo>cuarto and segundo>quinto:
    mayor=segundo
  elif tercero>primero and tercero>segundo and tercero>cuarto and tercero>quinto:
    mayor=tercero
  elif cuarto>primero and cuarto>segundo and cuarto>tercero and cuarto>quinto:
    mayor=cuarto
  else:
    mayor=quinto
  return mayor**menor
def raiz_cubica_del_menor_numero (primero:float,segundo:float,tercero:float,cuarto:float,quinto:float,menor:float) -> float:
  if primero<segundo and primero<tercero and primero<cuarto and primero<quinto:
    menor=primero
  elif segundo<primero and segundo<tercero and segundo<cuarto and segundo<quinto:
     menor=segundo
  elif tercero<primero and tercero<segundo and tercero<cuarto and tercero<quinto:
    menor=tercero
  elif cuarto<primero and cuarto<segundo and cuarto<tercero and cuarto<quinto:
    menor=cuarto
  else:
    menor=quinto
  return menor**(1/3)
if __name__=="__main__":
  menor:float=0
  mayor:float=0
  primero:int=int(input("Ingrese el primer numero: "))
  segundo:int=int(input("Ingrese el segundo numero: "))
  tercero:int=int(input("Ingrese el tercer numero: "))
  cuarto:int=int(input("Ingrese el cuarto numero: "))
  quinto:int=int(input("Ingrese el quinto numero: "))
  print("El promedio de los numeros es: "+str(promedio_numeros(primero,segundo,tercero,cuarto,quinto)))
  print("El promedio multiplicativo de los numeros es: "+str(promedio_multiplicativo_numeros(primero,segundo,tercero,cuarto,quinto)))
  print("La elevacion del mayor numero al menor numero es: "+str(numero_mayor_elevado_numero_menor(primero,segundo,tercero,cuarto,quinto,menor,mayor)))
  print("La raiz cubica del menor numero es: "+str(raiz_cubica_del_menor_numero(primero,segundo,tercero,cuarto,quinto,menor)))
```

5. #Consultar qué es y cómo funciona pip en python.

6. #Hacer un listado de módulos populares para python que se puedan instalar com pip y consultar cómo instalarlos.




