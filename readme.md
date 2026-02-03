## 🕹️ Retro BASIC Web Interpreter     
Un intérprete de lenguaje BASIC clásico moderno y ligero que se ejecuta completamente en el navegador. Este proyecto recrea la experiencia de programación de los ordenadores de 8 bits con una interfaz retro, soporte para gráficos y sintaxis extendida.    

![interprete](interprete.png)

## ✨ Características  
Sin dependencias:  
- Un único archivo HTML que contiene todo el código (CSS mediante Tailwind CDN).  
- Editor Integrado: Área de código con estilo retro.  
- Doble Salida:  
	- 📟 Terminal de Texto: Para comandos PRINT e INPUT.  
	- 🎨 Lienzo Gráfico (Canvas): Resolución de 256x256 para dibujar píxeles.  
- Sintaxis Clásica: Soporte para números de línea, GOTO, GOSUB, etc.  
- Ayuda Integrada: Modal con referencia rápida de comandos dentro de la aplicación.  
- Ejemplos: Varios programas precargados (Onda Senoidal, Fibonacci, Gráficos).  
  
## 🚀 Cómo usarlo  
1. Descargar: Clona este repositorio o descarga el archivo .html.  
2. Ejecutar: Abre el archivo basic_interpreter.html en cualquier navegador moderno (Chrome, Firefox, Edge, Safari).  
3. Programar: Escribe tu código BASIC en el editor de la izquierda.  
4. Correr: Pulsa el botón EJECUTAR para iniciar el programa.  
  
## 📖 Referencia del Lenguaje  
El intérprete soporta una versión simplificada pero potente de BASIC.  
  
**Control de Flujo**  
|Comando |	Descripción | 	Ejemplo |  
|---|---|---|  
|GOTO|	Salta a una línea específica|	10 GOTO 50|  
|IF...THEN	|Condicional simple	|20 IF X > 10 THEN GOTO 100|  
|FOR...NEXT	|Bucles (soporta STEP) | 30 FOR I=0 TO 10 STEP 2 ... 50 NEXT I|  
|GOSUB	|Llama a una subrutina |40 GOSUB 1000|  
|RETURN |	Vuelve de la subrutina | 1010 RETURN|  
|END |	Detiene el programa |999 END|  
  
**Entrada / Salida**  
|Comando|Descripción|Ejemplo|  
|---|---|---|  
|PRINT|Muestra texto o variables|10 PRINT "Hola " + NOMBRE|  
|INPUT|Pide datos al usuario|20 INPUT EDAD|  
|LET|Asigna valores (opcional)|30 LET A = 5 o 30 A = 5|  
|REM|Comentario|10 REM Esto es un comentario|


**Gráficos (Canvas 256x256)**
|Comando|Descripción|Ejemplo|  
|---|---|---|   
|PLOT X, Y|Dibuja un píxel|50 PLOT 128, 128|  
| COLOR "C"|Cambia el color del pincel|60 COLOR "red" o COLOR "#FF00FF"| 
| CLS| Limpia pantalla y terminal| 5 CLS| 

**Funciones Matemáticas**  
Se pueden usar dentro de expresiones o asignaciones LET.  
- SIN(x), COS(x), TAN(x): Trigonometría (en radianes).  
- SQR(x): Raíz cuadrada.  
- ABS(x): Valor absoluto.  
- INT(x): Parte entera.  
- RND(x): Número aleatorio entre 0 y x.  
- PI: Constante (3.14159...).  
  
**💻 Ejemplo de Código**  
Aquí tienes un pequeño programa para generar arte generativo simple:  
10 CLS  
20 PRINT "GENERANDO ARTE..."  
30 FOR I = 1 TO 500  
40 COLOR "cyan"  
50 IF RND(10) > 5 THEN COLOR "magenta"  
60 PLOT RND(255), RND(255)  
70 NEXT I  
80 PRINT "FINALIZADO" 

**🛠️ Tecnologías**
HTML5 Canvas: Para el renderizado gráfico.    
JavaScript (ES6+): Lógica del intérprete (lexer, parser y ejecución asíncrona).  
Tailwind CSS: Para el diseño de la interfaz de usuario.  

**📄 Licencia** 
este proyecto está bajo la Licencia GPL3  
  
**Autor:**  
Julio Sánchez Berro  
