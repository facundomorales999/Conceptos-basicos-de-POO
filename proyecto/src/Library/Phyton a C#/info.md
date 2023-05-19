Si sabes programar en Python, este documento puede servirte para saber cómo hacer en C# las cosas que ya sabes hacer. No es una referencia completa, sólo incluimos algunos aspectos de los lenguajes.

C# es un lenguaje compilado a lenguaje intermedio con tipos de datos estáticos.

Python es un lenguaje interpretado con tipos de datos dinámicos.

El ciclo habitual de desarrollo en C# implica editar uno o más archivos de código fuente, compilar los archivos de texto para producir un archivo binario en lenguaje intermedio, y ejecutar ese archivo binario en el entorno en tiempo de ejecución.

El ciclo habitual de desarrollo en Python implica ingresar una o más expresiones en un evaluador, que evalúa la expresión e imprime el resultado. También es posible desarrollar en Python editando uno o más archivos de código fuente, y ejecutar esos archivos con el intérprete de Python.

Los bloques de código en Python se definen mediante sangría en el código fuente, mientras que en C# se utiliza { al comienzo de un bloque y } al final.

Mientras es posible tener código Python en funciones o en métodos que pueden ser usados en expresiones, en C# el código sólo está en los métodos; no hay funciones “libres”. Algo análogo ocurre con las variables: mientras en Python puedo declarar variables globales, en C# las variables sólo pueden ser declaradas en las instancias de las clases, o en las propias clases; esto último equivale a las variables de instancia y de clase, respectivamente, que existen en Python.

Otras correspondencias o diferencias puedes encontrarlas en la tabla a continuación.

Python	C#
Comentarios en línea: #	Comentarios en línea: //
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
Comentarios en múltiples líneas comienzan y terminan con """	Comentarios en múltiples líneas comienzan con /* y terminan con */
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
if…, if…else, if…elif	if…, if…else, switch…case…default
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
for i in range(0, 3)…	for (int i = 0; i <=3; i++)…, foreach…
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
while (i < 3)…	while (i < 3)…
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
and, or, not	& y &&3,
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
<, <=, >, >=, ==, !=	<, <=, >, >=, ==, !=
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
+, -, *, /, +=, -=, *=, /=	+, -, *, /, +=, -=, *=, /=
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
bool	bool, Boolean
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
float	float, Single
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
int	int, Int32
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
str	string, String
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
Asignar el valor y a la variable x: x = y	Asignar el valor x a la variable y del tipo T: T x = y
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
Crear una instancia de una clase C y asignarla a la variable x: x = C()	Crear una instancia de una clase C
                                                                     |   y asignarla a la variable x: C x = new C();
-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------

float(…)	Convert.ToSingle(…), Single.Parse(…)
int(…)	Convert.ToInt32(…), Int32.Parse(…)
-------------------------------------------------------------------------	-------------------------------------------------------------------------------------------------------------------------------------------
str(…)	Int32.ToString(…), Single.ToString(…)
-------------------------------------------------------------------------	-------------------------------------------------------------------------------------------------------------------------------------------
Cuando demo es una variable que contiene una instancia de string, demo[0]	Cuando demo es una variable que contiene una instancia de String,
referencia el primer carácter, demo[-1] el último, demo[2:4]	demo[0] referencia el primer carácter, demo[^0] el último,
referencia una porción del segundo al cuarto carácter, y demo[:4]	demo[1..4] referencia una porción del segundo al cuarto carácte
                                                                     |  y demo[..4] una porción del primero al cuarto carácter
                                                                     |   
-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------- def… | No hay un solo equivalente en C#; para los métodos la sintaxis
| depende de la visibilidad, si retorna un resultado o no, | el tipo de datos del resultado, y otros factores. -------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------

class…	class…
self	this14
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
@classmethod	static
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
cls	El nombre de la clase
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
pass	Un bloque vacío {} o un ; puede ser similar en algunos casos,
                                                                     |   pero no existe una equivalencia exacta
-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------

raise…	throw…
with…	using…15 es similar, pero no existe una equivalencia exacta
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
print(…)	Console.WriteLine(…)
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
input()	Console.ReadLine()16
-------------------------------------------------------------------------	--------------------------------------------------------------------------------------------------------------------------------------------
assert…	Debug.Assert(…) es similar, pero se trata de una invocación
                                                                     |    y no de una palabra clave
-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------- yield | La palabra clave yield, existe en C#, pero no tiene exactamente | el mismo uso que en Python -------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------- import | No hay un equivalente exacto en C# porque los ensamblados | -análogos a los módulos o paquetes en Python- | sólo pueden ser cargados dinámicamente mediante una API, | a diferencia de Python que siempre son cargados dinámicamente. | using es una directiva en C# que permite referenciar | tipos en un espacio de nombres sin calificarlos.