------------------------------ Crear un programa------------------------------
 
			         
0-	mkdir proyecto	           	
1-	cd proyecto	            	
2-	mkdir src	                  
3-	cd src		         	
4-	dotnet new console -n Program
5-	dotnet new classlib -n Library
6-	cd Program	          	
	dotnet add Program.csproj reference ../Library/Library.csproj
7-	cd ..		                  		
8-	mkdir test	                   	
9-	cd test 	                   
	dotnet new nunit -n Library.Test		
10-	cd Library.Test                      				
	dotnet add Library.Test.csproj reference ../../Library.csproj

-------------------------------Ejecutar un programa------------------------------

cd src/Program
Compilar   dotnet build
Ejecutar   dotnet run

-------------------------------Repositorios--------------------------------------
				
Clonar			git clone
Mostrar ramas 		git branch
Crear rama 		git checkout -b
Actualizar rama		git pull
Para subir a la web		
	git add .		
	git commit -m "(Lo que voy a agregar)"
	git push
	
##------------------------------- Tarjetas CRC ------------------------------------
									________________________________________________
									|												|
									|					nombre						|
									|_______________________________________________|
									|						|						|
									|	responsabilidades	|		Clases que 		|
									|						|		contribuyen		|
									|_______________________|_______________________|


##-------------------------------PATRONES------------------------------------------

i) EXPERT:
	una clase debe tener la informacion necesaria para cumplir con su responsabilidad

ii) POLIMORFISMO:
	una operacion es polimorfica cuando implementa dos o mas objetos de diferentes tipos

iii) Creator:
	Quien deberia ser responsable de crear una nueva instancia de cierta clase?

Asignar a la clase b la responsabilidad de crear una instancia de la clase a si una de las siguientes
		B agrega objetos de A
		B contiende objetos A
		B guarda instancias de objetos A
		B usa de forma muy cercana objetos A
		B tiene los datos que seran provistos al constructor para inicializar instancias de A por lo que B es experto con respecto a crar A

iv) Acoplamiento bajo y alta cohersion:
		1)
	El acoplamiento es una medida de qué tanto o de qué tan fuertemente una clase está conectada con otra, o depende de la otra. Una clase con poco acoplamiento o con acoplamiento bajo no depende de muchas otras clases; Como regla general, cuánto más bajo el acoplamiento, mejor. La forma de crear acoplamiento entre clases es cuando una clase depende de la otra:
	Una clase es una subclase de la otra.
	Una clase tiene una variable de instancia o un atributo que es un objeto o una colección de objetos de la otra.
	Una clase tiene un método que retorna o que recibe como argumento un objeto de la otra clase.
	Una clase crea un objeto de la otra clase internamente en un método.
		2)
	la cohesión es una medida de qué tan enfocadas y fuertemente relacionadas están las responsabilidades de una clase. Una clase con responsabilidades alta o fuertemente relacionadas tiene alta cohesión.  Por el contrario, una clase con baja o poca cohesión hace muchas cosas que no tienen que ver entre sí. Como regla general, cuanto mayor es la cohesión, mejor.


v) LEY DE DEMETER:
	Cada unidad debe tener un limitado conocimiento sobre otras unidades y solo conocer aquellas unidades estrechamente relacionadas con la unidad actual. Cada unidad debe hablar solo a sus amigos y no hablar con extraños.




-------------------------------PRINCIPIOS----------------------------------------


i) SRP
	Una responsabilidad es considerada un motivo de cambio.
	Este principio establece que si tenemos 2 motivos de cambio, debemos dividir la funcionalidad en dos clases. Cada clase debe tener responsabilidad sobre una parte de la funcionalidad proporcionada por el software, y la responsabilidad debe estar completamente encapsulada por la clase.

ii) OCP
	Las clases1 deben ser abiertas a la extensión, pero cerradas a la modificación.

	Que una clase sea “abierta a la extensión” quiere decir que las responsabilidades de la clase pueden ser extendidas se puede agregar nuevas responsabilidades mediante herencia o mediante una combinación de herencia y composición o agregación.

	Que una clase es “cerrada a la modificación” quiere decir que no es posible y no es necesario si se cumple el principio realizar cambios en el código de esa clase.

iii) LSP
	Establece que si un módulo del programa usa una clase base, entonces la referencia a la clase base se puede reemplazar con una clase derivada sin
	Patrones y principios 2 afectar la funcionalidad del módulo del programa. Debemos asegurarnos que las nuevas clases derivadas simplemente se extiendan sin reemplazar la funcionalidad de las clases antiguas. De lo contrario, las nuevas clases pueden producir efectos no deseados cuando se utilizan en módulos de programa existentes. En resumidas cuentas: los subtipos deben ser completamente sustituibles por sus supertipos.

iv) ISP
	ISP establece que no se debe obligar a los clientes a implementar interfaces que no utilicen. En lugar de una gran interfaz, se prefieren muchas interfaces pequeñas basadas en grupos de métodos, cada una de las cuales sirve a un submódulo.
	En resumen: "los clientes no deben ser forzados a depender de tipos que no usan".
	Si se aplica más de lo necesario, resultará en un código que contiene muchas interfaces con métodos únicos, por lo que la aplicación debe realizarse en base a la experiencia y el sentido común para identificar las
	áreas donde es más probable que ocurra la extensión del código en el futuro.

v) DIP
	Las clases2 de alto nivel no deben depender de clases de bajo nivel; ambas deben depender de abstracciones.
	Las abstracciones no deben depender de detalles; los detalles deben depender de abstracciones	

-------------------------------Diagramas de Clase--------------------------------
													_________________________
nombre de la clase									|	Nombre de la clase	|
													|_______________________|
- private						 					|variables de instancia	|
+ public											|_______________________|
													|		   				|
-----> dependencia (punteada)						|	constructores	   	|
------ Asociacion  (linea recta)					|_______________________|
------> Herencia (linea sin puntear)
-------- Agregacion (con el rombo claro)
-------- composicion (con el rombo oscuro

------------------------------- Herencia--------------------------------------



	La herencia es un mecanismo de los lenguajes de programación para implementar declarativamente relaciones de generalización entre una o más clases bases y una o más clases sucesoras.
	Forma de reutilizar codigo


Singleton:
	es para crear instancias unicas de un objeto


------------------------------ Tipos -----------------------------------------

Tipo:
	Un tipo es un conjunto de operaciones que determina los mensajes que pueden ser enviados a los objetos de ese tipo. 


