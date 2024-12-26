# Asuma que el pinguno es un cilindro
En este repositorio se socializara el recorrido para cumplir con el reto 5

## 1. 

![Ejercicio 1](https://camo.githubusercontent.com/9a79fe9629fff1ceecb5860dba4054b90da7acda3d4f2c9cd7f62a34799894d2/68747470733a2f2f692e706f7374696d672e63632f465276436d7078782f696d6167652e706e67)


### 1) Calcular volumen y area superficial (matematica)

Volumen: 
```
(4/3)*pi*r1**3+pi*r2**2*h*(1/3)
```

Area:
```
4*pi*r1**2+pi*r2**2+pi*r2*((r2**2+h**2)**0.5)
```

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

![Ejercicio 2](https://camo.githubusercontent.com/1e035694c4675debe6703e3771f67ff06d8da330997d02c3806aa2bd5936bc54/68747470733a2f2f692e706f7374696d672e63632f3174344d727a734c2f696d6167652e706e67)

### 1) Calcular area y perimetro (matematica):

Area: 
```
b*a+2*r**2*pi
```
Perimetro:
```
2b+2a+2*(2*pi*r)
```
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

6. #Consultar qué es y cómo funciona pip en python.

  El nombre de pip, en python, corresponde a un acronimo que viene de: pip Install Packages (on instalador de paquetes pip, en español).
  pero

  ¿Que son los paquetes en python? 
  Comenzemos por dar contexto, en python, se utilizan muchas operaciones, de suma, de resta, de igualdad, de desigualdad, etc. Y cuando ya se tiene un tiempo programando, es facil darse cuenta que la forma de "programar" estas operaciones pueden definirse como algoritmos, entonces, ya se plantea una estructura detallada, se tiene la idea de como hacerla cada vez que se requiera y se ahorra el tiempo de tomarse el trabajo de "redefinir" los conceptos de la programcion y la mecanizacion de procesos; Simplemente se tiene un "estandar", pero luego de nuevo con pensamiento critico y propositivo, se llega a la conclusion de que estos algoritmos pueden ser funciones estandarizadas, entonces se define una funcion con la capacidad de "replicar" ese algortimo cada vez que se necesite, y ahora, se tiene la posibilidad de simplementa llamar la funcion cuando se necesite y ahorrarse reescribir el algoritmo cada vez; De igual manera, con mas tiempo y pensamiento critico y propostivo, se dara cuenta que la definicion de estas funciones entre programas es un proceso repetitivo y facilmente transformable a un algoritmo, de modo que ahora, se crearan algo llamado LIBRERIAS/BIBLIOTECAS (o LIBRARIES en ingles), que contienen todas esas funciones definidas (con sus respectivas transformaciones para que funcionen en cuaquier programa), de manera que ahora, no tengo que pensar en como podria restar dos numeros, tampoco tengo que escribir repetidas veces este proceso, ni tengo que definir una funcion con la operacion cada vez que la necesite (en cada programa), y tan solo necesitare importar la libreria cada vez que necesite esa operacion especifica; Este metodo de las librerias es lo que hizo muy populares a lenguajes como python y c, por su practicidad y utilidad.
  
  ¿De donde vienen las librerias?
  Las librerias vienen en paquetes que traen lo necesario para que funcionen luego de instalarse, cosas como los archivos relacionados, los modulos de la libreria (o paquete), y demas dependencias que requiera la libreria; Estos pueden encontrarse de dos formas, primero, como es facil imaginarselo, en internet se suben las librerias para que esten a disposicion del publico (la mayoria de uso gratuito) en algunas paginas que recopilan estas librerias aceptadas por la comunidad de python, tales como: [Python Package Index (PyPi)](https://pypi.org/) o [Anaconda](https://anaconda.org/anaconda/repo); Adicionalmente a las librerias que ya estan dentro de internet, python trae por defecto una libreria ya instalada llamada [Python Standard Library](https://docs.python.org/3/library/), esta contiene soluciones a los problemas diarios de la programcion en forma de las librerias instaladas que pueden ser importadas sin necesidad de instalar o hacer algun proceso adicional.
  
  ¿Para que necesito un instalador?
    Como ya se menciono, python trae una libreria por defecto, que permite importar sin pasos extra, y ese misma caracteristica de evitar pasos extra, es para lo que funcionma el instalador, te evita de tener que buscar donde estan los archivos, apilarlos, ordenarlos, relacionarlos, adaptarlos a tu python, agregar las cosas que sean necesarias para que funcionen (dependencias), actualizarlos (y lo que conlleve), configurarlos (y lo que conlleve), borrarlos (y lo que conlleve) etc. Simplemente se le da la orden de que instale la libreria y lo necesario para ella, y el hara el resto del trabajo, por lo tanto es eficiente, util, y amigable con quien lo necesite, para que no deba volverse un experto en ese tema, simplemente viene a conseguir una biblioteca, y eso lo ayudara a hacer solamente eso; ¿Y como se relaciona esto con el pip? El pip es precisamente eso, una herramienta que gestiona la descaerga e instalacion de paquetes y sus complementos de python (y las mas popular).

  ¿Como uso pip?
  Tomando el caso de que ya se haya comprobado que se tenga pip instalado y el python 3+ instalado y ejectuado por defecto en simbolo del sistema con el comando ``` python --version ``` (la version que le sea pertinente instalar, en este curso utilizamos python 3+, por lo que se explicara para esa version) y el nombre de la biblioteca deseada encontrado, solo se ingresa al simbolo del sistema y desde ahi se coloca la siguiente estructura:

```
pip install nombre_del_paquete
```
En caso de que solo se tenga una version de python instalada

o

```
python3 -m pip install nombre_del_paquete (por ejemplo frutas)
```

Tambien es probable que se necesite instalar una version especfica del paquete y esto pip, lo permite, usando la siguiente estructura:

```
pip install nombre_del_paquete==version_deseada (por ejemplo 1.4.2)
```

O quizaz sea pertinente instalar una verison que este entre otras, pip, permite hace esto, y lo hace a travez del uso de logica de booleanos, asi:

```
pip install nombre_del_paquete>=condicion,<otra_condicion
```

Los paquetes tienen algo llamado dependencias, que son basicamente mas paquetes que el paquete principal necesita para funcionar y son descargados automaticamente por pip, como en el siguiente ejemplo, instalando scikit-learn:

```
pip install Scikit-learn
```

![image](https://github.com/user-attachments/assets/a0dd1862-90d0-497e-a9a8-792e8c332eb3)

Aqui se nota como es que ademas de descargar el paquete de scikit-learn descarga las dependencias adicionales de Scikit-learn

Cuando se trabaja en equipo, muchas veces es necesario que se instalen las mismas librerias y versiones, esto se puede hacer teniendo una lista de las librerias y sus verisiones e ir instalando una por una cada persona, pero.... como siempre, esto puede ser un algoritmo y pip lo aprueba, porque tiene una funcion que admite recibir un documento de texto (generalmente llamado requirements) que tenga las librerias y sus versiones e instalarlas, esto funciona con la siguiente estructura (el archivo de texto debe estar dentro del rango de accion del ambiente virtual en el que se abre el simbolo del sistema): 

(dentro del documento de texto debe estar:
nombre__del_paquete==version_deseada
nombre__del_paquete2==version_deseada
nombre__del_paquete3==version_deseada

```
pip install -r nombre_del_archivo.txt
```

De igual manera, sino quieres hacer la lista cada vez que la necesites, podrias instalar los paquetes que necesites y usar:

```
pip freeze > nombre_del_archivo.txt
```

Si se quiere visualizar los paquetes instalados en el ambiente virtual antes de crear la lista, se usa:

```
pip list
```

Esto generara un archivo de texto de nombre "nombre_del_archivo" que podra ser compartido con los demas compañeros

Tambien es comun que se deban actualizar los paquetes de instalacion, por lo que se podra usar el siguiente comando para actualizarlas:

```
pip install --upgrade nombre_del_archivo
```

Asi tambien los archivos de paquetes de instalacion pueden ser usados para actualizar cada paquete especificado en el, hecho asi:

```
pip install -r requirements.txt --upgrade
```

El pip, tambien permite borrar paquetes de instalacion usando:

```
pip uninstall nombre_del_paquete
```

De igual manera se puede hacer con las listas

```
pip uninstall -r nombre_del_archivo.txt
```

(Lo siguiente no lo tengo tan claro en su funcionamiento, pero si su teoria)
Github es una de las plataformas (ademas de las ya mencionadas) que pueden alojar los paquetes en python, y pip permite instalarlos desde ahi, simplemente se necesita encontrar el respositorio que tenga el paquete que requerido y el ejecutable funcional para instalarlo, siendo asi su estructura (solo para descargarlo directamente desde un respositorio, si se quiere hacerlo en una rama, una version especifica o un commit especifico, se tendra que usar otro metodo):

```
pip install git+https://github.com/usuario/nombre_respositorio.git
```

  Adicionalmente, si se llegar a necesitar una especificacion de los distintos comandos que tiene pip, se puede usar:

```
pip help
```

  Si se quiere ver el resumen de un paquete se usa:

```
pip show [nombre_del_paquete]
```

  A pesar de lo extraño que pueda ser, es posible que pip no este instalado (a pesar de tener python instalado), esto generalmente sucede por tener una version antigua de python (pip viene generalmente instalado desde 2.7.9 y 3.4, hacia adelante) y se puede corregir instalando el pip, con el siguiente codigo (de nuevo solo se explica para python 3+ pues es lo pertinente para el curso):

```
  python3 -m ensurepip --default-pip
```

  Algo mas comun de encontrar es que el pip no este actualizado a la ultima version, esto se puede solucionar con el siguiente codigo:

```
pip install –upgrade pip setuptools wheel
```

  La informacion anteriormente descrita la obtuve a partir de [esta](https://www.datacamp.com/tutorial/pip-python-package-manager#rdl) pagina web, la recomiendo, explica muy bien el tema y si se quiere explorar un poco mas, es excelente

7. #Hacer un listado de módulos populares para python que se puedan instalar com pip y consultar cómo instalarlos.

(Hay otro ejemplo de instalar bibliotecas populares en donde se explica que los paquetes tienen dependencias, es la instalacion de Scikit-learn)

[Librerias de python](https://immune.institute/blog/librerias-python-que-son/)

PyTorch
Es una libreria que es usada para las redes neuronales, esta compuesta de 3 partes principales, torch "el principal" (Núcleo principal de PyTorch para tensores y redes neuronales), torchvision (Herramientas para visión por computadora (datasets, modelos, transformaciones)) y torchaudio (Herramientas para procesamiento de audio (datasets, transformaciones, modelos)); Se puede instalar solo uno o el principal y alguno en especifico, o todos directamente, aqui se presentaran todos directamente para mostrar que se pueden instalar varios al mismo tiempo (esto con el fin de que todos se instalen en la misma version, evitando asi problemas de compatibilidad):

Codigo para instalarlo: 

```
pip install torch torchvision torchaudio
```

Pandas
Es una libreria ampliamente usada en ciencia de datos, la cual provee estructuras de datos expresivas para que sea sencillo e intituivo trabajar con ellas

Codigo para instalarlo: 

```
pip install pandas
```

NumPy
Es una libreria usada en ciencia de datos para tener arreglos de tamaño n y trabaja sobre ellas, tiene vectores multidimensionales

Codigo para instalarlo:

```
pip install numpy
```
