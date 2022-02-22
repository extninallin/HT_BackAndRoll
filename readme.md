# Instalar módulos Python para el script
Para realizar la instalacion de todas las depencias que necesita el **HT_BackAndRoll.py** y **do_requests.py** debemos tener instalado **Python** (scripts hechos en **version 3.10.1**) y **pip** (version **22.0.3**), ejecutar el siguiente comando en la consola:
```
pip install -r requirements.txt
```
Luego de todo instalar ejecutar (o Ctrl+F5) dentro del scipt **HT_BackAndRoll.py**

# Input
El input se tiene que crear en un archivo .csv con el listado de todos los sellers que se necesita hacer el backup o el roll. Este mismo puede guardarse dentro de la carpeta donde esta el programa o en otra.

ejemplos:

 **sellers_MLB_XD_SSHP-370151.csv**

 **sellers.csv**

 **sellers_MLA_XD.csv**

```
757566993
754487423
754487209
1044760013
....
```
# Pantalla del programa

### 1_Debemos buscar el archivo .csv con el "Browse"

![](/images/front.PNG)

### 2_Luego debemos especificar en las listas desplegables el Site, Logistic type y la Opcion (Backup/Rollback)

![](/images/front_1.PNG)

### 3_Al apretar Ok nos aparece una pantalla detallando y preguntando si los datos son los correctos
![](/images/front_2.PNG)

### 4_Una vez concluido nos informa que debemos controlar en la carpeta donde se encuentra el script y encontraremos un archivo "_BAK", con el listado de los sellers y sus payloads
![](/images/front_3.PNG)

# Rollback
Para realizar un Rollback lo que difiere es en el browse del archivo, ya que antes buscabamos un archivo .csv ahora debemos cambiar la busqueda por un .txt. Y debemos cargar este .txt (el cual tiene un formato predefinido con un _BAK), se completa los campos requeridos cambiando la opcion a RollBack, una vez realizado el rollback, como buena practica, se debe controlar por postman si el impacto se realizo (o descargarse nuevamente un backup y controlar si coincide con lo impacto hace un momento).