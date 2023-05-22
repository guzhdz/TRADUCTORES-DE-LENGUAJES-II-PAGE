# Compilador

Un traductor es un programa que recibe como entrada código escrito en un cierto lenguaje y produce como salida código en otro lenguaje.

https://sciatel.wikispaces.com/TRADUCTORES+DEL+LENGUAJE+DE+PROGRAMACION

Un compilador es un programa informático que traduce un programa que ha sido escrito en un lenguaje de programación a un lenguaje común, usualmente lenguaje de máquina, aunque también puede ser traducido a un código intermedio (bytecode) o a texto. Este proceso de traducción se conoce como compilación.

https://es.wikipedia.org/wiki/Compilador

# Analizador Lexico
Link: https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/tree/main/Proyecto%20principal%20(Por%20partes)/Analizador%20Lexico

El Análisis Léxico es la primera fase de un compilador, este consiste en un programa que recibe como entrada el código fuente de otro programa (secuencia de caracteres) y produce una salida compuesta de tokens (componentes léxicos) o símbolos. 

# Tarea: Mini generador léxico 
Genera un pequeño analizador léxico, que identifique los siguientes tokens (identificadores y números reales) construidos de la siguiente manera.
identificadores = letra(letra|digito)*
Real = entero.entero+

El codigo se encuentra en los archivos script.js y analizador.js, para ejecutarlos puede simplemente compilar y correr el archivo script.js o usar la extension de live server de VS Code para hacer deploy del index.html y en consola ver el resultado de la ejecucion.

Resultado de la ejecucion:
![Mini analizador img 1](https://user-images.githubusercontent.com/89165084/213944343-8f33242a-b181-4698-93a7-c2b1be2fcc3a.jpg)
![Mini analizador img 2](https://user-images.githubusercontent.com/89165084/213944420-bc4f6c95-de59-4618-8b0c-914a9ce720c0.jpg)


# Tarea: Etapa del proyecto analizador léxico completo.
Genera un analizador léxico utilizando todos los símbolos léxicos en el archivo simbolos_lexicos.pdf.

Resultado de la ejecucion:

![Analizador completo img 1](https://user-images.githubusercontent.com/89165084/213944726-ec851892-1ca3-4041-afac-36f8ae2a7296.jpg)!
![Analizador completo img 2](https://user-images.githubusercontent.com/89165084/213944892-50c32dfd-bedf-4cc9-b39f-dbef5ddffcfc.jpg)!

Se mejoro el aspecto visual, de manera que ahora si se ejecuta en un servidor local o con la extension live server de visual code el archivo index.html, aparecera una interfaz visual que permitira ingresar cualquier texto y lo analizara:

![Lexico visual1](https://user-images.githubusercontent.com/89165084/216058211-45b5e04a-d30b-4e36-8872-c6eb2074101f.jpg)

![Lexico visual2](https://user-images.githubusercontent.com/89165084/216058237-a12973df-fb88-4dd8-a91e-8b2237fc4bcb.jpg)

# Analizador sintactico
Un analizador sintáctico, es un programa informático que analiza una cadena de símbolos según las reglas de una gramática formal. El análisis sintáctico convierte el texto de entrada en otras estructuras (comúnmente árboles), que son más útiles para el posterior análisis y capturan la jerarquía implícita de la entrada. 

Un analizador léxico crea tokens de una secuencia de caracteres de entrada y son estos tokens los que son procesados por el analizador sintáctico para construir la estructura de datos, por ejemplo un árbol de análisis o árboles de sintaxis abstracta. 

El uso más común de los analizadores sintácticos es como parte de la fase de análisis de los compiladores. De modo que tienen que analizar el código fuente del lenguaje, los lenguajes de programación tienden a basarse en gramáticas libres de contexto, debido a que se pueden escribir analizadores rápidos y eficientes para estas.

# Tarea: Mini analizador sintáctico (Excel)
Subir un archivo en excel simulando las gramáticas del ejercicio 1 y 2 del archivo (Practica Analizador Sintactico LR.pdf)

Entrada para el Ejercicio 1
hola+mundo

Entrada para el Ejercicio 2
a+b+c+d+e+f

Link de archivo: https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/blob/main/Tareas/Tarea%202.%20Mini%20analizador%20sintactico/Mini%20analizador%20sint%C3%A1ctico%20(Excel).pdf

# Tarea: Mini analizador sintáctico (código)
Generar un algoritmo para analizar los Ejercicios 1 y 2 del archivo (PracticaAnalizadorSintactico.pdf)

Se modifico el codigo del analizador lexico para que funcionara junto con un codigo nuevo y hicira la funcion del analizador sintactico. Se agrego una nueva clase (Sintactico) la cual realiza as tareas importantes del mismo, ademas de que se cambio la interfaz para que concordara con el objetivo de este mini analizador sintactico.

Link del proyecto: https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/tree/main/Tareas/Tarea%202.%20Mini%20analizador%20sintactico/Mini%20analizador%20sintactico%20programa

El proyecto puede ejecutarse en un servidor local o mediante la extension de live server de visual code, ejecutando el index.html.

Foto del codigo:

![image](https://user-images.githubusercontent.com/89165084/216158896-8cb0f7ee-7cd4-4c8a-90ed-876efc65695e.png)

Tablas LR en las que se baso el codigo:

![image](https://user-images.githubusercontent.com/89165084/216159161-9e1cdc1b-b374-48d8-aeab-01dfb023f9de.png)

![image](https://user-images.githubusercontent.com/89165084/216159390-5e52721e-aa6b-4729-9a4d-fd20a71e23b5.png)

Prueba y ejecucion del codigo del Ejercicio 1:

![image](https://user-images.githubusercontent.com/89165084/216159777-45f6c593-721b-4c14-93fb-43335ffb41c9.png)

Prueba y ejecucion del codigo del Ejercicio 2:

![image](https://user-images.githubusercontent.com/89165084/216160956-22bb9bee-eb72-49fd-bfa2-d0586d7a0fb6.png)
![image](https://user-images.githubusercontent.com/89165084/216161014-4494532f-6c4b-41e3-bd81-e439b35aa6ef.png)
![image](https://user-images.githubusercontent.com/89165084/216161151-3f58e151-f901-40c1-aa00-9b7019499237.png)

# Tarea: Gramática del compilador
Utilizando tu analizador léxico y tu algoritmo para trabajar con las tablas lr. Carga e implementa la siguiente gramática.
(Los archivos de la garmatica esten en: https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/tree/main/Proyecto%20principal/GramaticaCompilador)

Se modifico el codigo de la clase sintactico para que de esta manera la gramatica y tabla LR que utilizara de base fuera la dada en los archivos de la nueva
gramatica, se hizo de manera que que se leyera el archivo cada que se construyera el objeto y en sus arreglos copiaba la tabla:

![image](https://user-images.githubusercontent.com/89165084/219900764-6460108c-7108-41ce-b941-c14067921367.png)

Ademas se cambio visualmente la interfaz del programa, ahora enfocandose en el analisis sintactico y cambiando el input por yn textarea, asi el usuario puede
ingresar un programa:

![image](https://user-images.githubusercontent.com/89165084/219900924-ad395dbe-7274-43ee-a2d4-164bcb39291a.png)

Ejecucion:

![image](https://user-images.githubusercontent.com/89165084/219900948-4348fa38-aaac-45fb-a270-91b6bfda7bd0.png)

![image](https://user-images.githubusercontent.com/89165084/219900969-cc45ffc5-bb61-499d-8645-c6ac39edf9d5.png)

Para proposito de que no terminara muy larga la explicacion solo se tomo captura del inicio y final de la tabla

# Arbol sintactico

El Árbol de sintaxis abstracta es una estructura de datos usada extensamente en compiladores, debido a su propiedad de representar la estructura del código de un programa. Un AST es usualmente el resultado del analizador sintáctico en la fase de un compilador. A menudo sirve como un intermediario de la representación del programa a través de etapas que requiere el compilador, y tiene un impacto fuerte en la salida final del compilador.

# Tarea: Ejemplo gramática LR utilizando tabla de compilador.

Se modifico el codigo de la clase sintactico para que se creara un arbol sintactico mientras se va realizando el analisis y asi guardar cada parte del codigo a analizar,
se crearon las clases necesarias para el arbol, una por cada regla, una siendo el nodo y las ultimas dos siendo el arbol y una que controlara todas.

![image](https://user-images.githubusercontent.com/89165084/224136832-d4bca03e-445e-4c20-8350-0a59caba4b80.png)

![image](https://user-images.githubusercontent.com/89165084/224136929-58835ee3-8954-495d-9a7d-38f99ca125f0.png)

Al final se agrego codigo en el script.js donde se imprime el arbol despues de realizar el analisis, probemos con el ejemplo int hola; :

![image](https://user-images.githubusercontent.com/89165084/224136601-0b05f6b2-b49b-49a4-8772-932d62dddadd.png)

![image](https://user-images.githubusercontent.com/89165084/224136677-781e542e-5a15-4b72-923b-19b00ea183c9.png)

Como se observa se muestra el arbol y el numero indica el nivel e cada nodo.

# Analizador Semantico

Un analizador semántico es una herramienta utilizada en el procesamiento de lenguaje natural y la compilación de programas informáticos. Su función principal es analizar la estructura sintáctica de una oración o expresión, y asignar significado a las palabras y elementos presentes en la misma.
En el caso de la compilación de programas informáticos, el analizador semántico se utiliza para validar la corrección de la sintaxis de un programa y verificar que las variables y operaciones utilizadas tengan sentido en el contexto del lenguaje de programación utilizado. Por ejemplo, si se utiliza una variable que no ha sido declarada previamente, el analizador semántico detectará el error y lo reportará.

![image](https://user-images.githubusercontent.com/89165084/230996230-38d2e05f-9757-4d8a-a2ca-d5e657be37c9.png)

Si ejecutamos el programa nos presenta el modelo visual que ya concoemos de un textArea y un boton, en este caso al analizar la entrada nos despliega el arbol sintactico y ademas nos dice si la estrada es aceptada o si ocurre algun error semantico, ademas de que nos indica cual.

Interfaz:

![image](https://user-images.githubusercontent.com/89165084/230996740-fd265b6f-8b60-4db3-ac46-284473ce74e8.png)

Prueba con codigo bien:

![image](https://user-images.githubusercontent.com/89165084/230996872-c0ad5f1d-81c9-4dca-9c76-f69719c9cb8b.png)

Arbol sintactico:

![image](https://user-images.githubusercontent.com/89165084/230997003-20e2dd52-5d5f-462a-a7e9-50873540dfea.png)

Prueba con error:

![image](https://user-images.githubusercontent.com/89165084/230997165-ec9eab4e-7152-4b49-9e15-b1346c461fd2.png)

# Generador de codigo
Un generador de código es una herramienta o recurso que genera un tipo particular de código o lenguaje de programación de computadora. Esto tiene muchos significados específicos en el mundo de TI, muchos de ellos relacionados con los procesos a veces complejos de convertir la sintaxis de programación humana al lenguaje de máquina que puede leer un sistema informático.

# Tarea: Generador e codigo
Utilizando tu arbol sintactico y con el previo analisis semanticos codifica un algoritmo que genere un codigo en lensuaje ensamblador que pueda ser ejecutado por un emulador o programa ensamblador.

Se modifico el proyecto agregando al clase genCode, dicha clase se encarga de recorrer por seguna vez el arbol sintactico esta vez no para analizarlo si no que lo realiza para escribir codigo en un archivo, este codigo representa la escrito por el usuario y lo tranforma en leguaje ensamblador, plasmandolo mediante un arreglo de strings que despues mediante un objeto Blob el cual construye el archivo con termiancion .asm listo para descargar y ejecutarlo en procesador o un emulador.

![image](https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/assets/89165084/9e50b2a7-698b-4ce6-948b-383854c2be13)

Ademas se cambio visualmente la interfaz del programa, ahora enfocandose en la geenracion del codigo, ademas de añadir el boton de descargar cuando el codigo sea ingresado correctamente y termine de geenrar el archivo .asm:

![image](https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/assets/89165084/44e88525-7b81-4100-8ab7-66ef0ad9e968)


Ejecucion:

![image](https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/assets/89165084/e270def9-455c-485b-9525-8f18f31b0678)

![image](https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/assets/89165084/1cb63a17-299f-48d0-92a5-f284811b3a52)

![image](https://github.com/guzhdz/TRADUCTORES-DE-LENGUAJES-II/assets/89165084/b82c9c3d-4dc4-4749-b039-f232ff152d88)


