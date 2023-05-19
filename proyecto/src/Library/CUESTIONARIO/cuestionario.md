Pregunta 1

    Enunciado de la pregunta
    A la clase Drawer, se le ha asignado la responsabilidad de dibujar figuras geométricas:

    *IMAGEN 1*

    Sin embargo, esta implementación no cumple con el principio ISP :x: ya que si queremos dibujar una nueva figura, por ejemplo un triángulo, debemos  Modificar :white_check_mark: la clase Drawer.

Pregunta 2

    ¿Cuándo una operación es polimórfica?

    a.
    Cuando es implementada por dos o más objetos de diferentes tipos
                                    :white_check_mark:

    b.
    Cuando no la implementa ningún objeto
                                    :x:
    c.
    Cuando es implementada por un objeto de dos o más tipos
                                    :x:
    d.
    Cuando es implementada por un objeto de un tipo
                                    :x:


Pregunta 3

    ¿Cómo se traduce a código C# la expresión en lenguaje natural "la clase XmlNotFoundException es un sucesor de Exception"?


    Seleccione una:

    a.
    public class XmlNotFoundException inherits Exception
    {
        …
    }
                        :x:

    b.
    public class Exception : XmlNotFoundException 
    {
        …
    }
                        :x:

    c.
    public class Exception inherits XmlNotFoundException 
    {
        …
    }
                        :x:
    d.
    public class XmlNotFoundException : Exception
    {
        …
    }
                        :white_check_mark:


Pregunta 4

    En el siguiente diagrama:

                *IMAGEN 2*

    Las clases ConsolePrinter y FilePrinter Respuesta
    Implementan :white_check_mark:

    la interfaz IPrinter. La operación PrintTicket es una operación Respuesta
    Sobrecargada :x:
    Polimorfica :white_check_mark:



Pregunta 5

    Sea el siguiente código:

    public void StartBot(IBot bot)
    {
        
        var cts = new CancellationTokenSource();

        bot.Start(new DefaultUpdateHandler(HandleUpdateAsync, HandleErrorAsync));

        bot.CancellationToken = cts;
    }

    Aunque no sabemos qué tipo es el objeto referenciado en la variable bot, solamente mirando este fragmento de código, ¿qué métodos y/o propiedades podemos deducir que tiene?

    Método, sería Start únicamente 

    Comentarios
    Método, sería Start únicamente.  :white_check_mark:

Pregunta 6

    Enunciado de la pregunta
    El patrón Don't Talk To Strangers, también conocido como Ley de Demeter, dice que hay que asignar la responsabilidad de colaborar con objetos indirectos de un objeto dado a los objetos directos, para que ese objeto no necesite conocer a los objetos indirectos. En este contexto, un objeto directo de un objeto dado es:

    Seleccione una o más de una:

    a. Un objeto creado dentro de un método.                                    :white_check_mark:

    b. Un objeto contenido en una colección del propio objeto.                  :white_check_mark:

    c. Un objeto recibido como argumento en un método del propio objeto.        :white_check_mark:

    d. Un atributo del propio objeto.                                           :white_check_mark:

    e. El propio objeto -this en C#-.                                           :white_check_mark:


Pregunta 7

    Teniendo en cuenta la siguiente clases con sus responsabilidad y colaboraciones:

        *IMAGEN 3*

    Indicar si se cumple el principio SRP. En caso negativo, indicar qué responsabilidad deberíamos quitar de la clase para que se cumpla el principio.

    a.
    Conocer el material ofrecido
                                                        :x:
    b.
    Conocer fecha y hora de la publicación
                                                        :x:
    c.
    Sí, cumple con SRP.
                                                        :x:
    d.
    Responder comando /listar de Telegram
                                                        :white_check_mark:

    e.
    Conocer la ubicación del material
                                                        :x:

Pregunta 8

    Completa el siguiente cuadro comparativo de reutilización basada en herencia versus reutilización basada en composición y delegación: para una característica o afirmación, marca la casilla de herencia o la de composición, si esa característica o afirmación se aplica a una o a la otra respectivamente:

    Reutilización de caja negra:
                        Composición :white_check_mark:                    	Herencia :x:


    Reutilización de caja blanca:
                        Composición :x:	                                    Herencia :white_check_mark:
   

    Relación dinámica, en tiempo de ejecución:
                        Composición :white_check_mark: 	                    Herencia :x:
    

    Relación estática, en tiempo de compilación:
                        Composición	                                        Herencia :white_check_mark:
 

    Relación establecida con líneas de código:
                        Composición :white_check_mark:	                    Herencia :x:


    Relación declarativa:
                        Composición	                                        Herencia :white_check_mark:
    

    Reutilización más selectiva:
                        Composición :white_check_mark: 	                    Herencia :x:
  
  
    Reutilización de tipo todo o nada:
                        Composición	                                        Herencia :white_check_mark:


    No hay relación entre el tipo reutilizado y el que reutiliza:
                        Composición :white_check_mark:                      Herencia :x:
   

    El tipo que reutiliza es un subtipo del tipo reutilizado:
                        Composición	                                        Herencia :white_check_mark:
    

Pregunta 9

    En el siguiente diagrama:

        *IMAGEN 4*

    DiscLibrary contiene múltiples instancias de Disc, este tipo de relaciones se llama Respuesta
    Agregación :white_check_mark:



Pregunta 10

    Sea el siguiente código

    public interface IPrinter
    {
        void PrintTicket(Sale sale);
    }
    public class TimeMachinePrinter : IPrinter
    {
        public void PrintTicket(Sale sale)
        {
            sale.DateTime = new DateTime(2001, 01, 01);
            Console.WriteLine(sale.GetTextToPrint());
        }
    }

    public static void Main(string[] args) {
            ...
            Sale sale = new Sale();
            ...
            IPrinter printer;
            printer = new ConsolePrinter();
            printer.PrintTicket(sale);
            printer = new FilePrinter();
            printer.PrintTicket(sale);
    }
    
    ¿Se puede decir que TimeMachinePrinter cumple con el LSP? La implementación de ConsolePrinter y FilePrinter se omiten por simplicidad

        Seleccione una:

        a.
        Si, porque la operación es polimórfica. Por lo tanto si es polimórfica se cumple el LSP
                                :x:

        b.
        Ninguna es correcta. 
                                :x:

        c.
        No, porque cambia la fecha de la compra. No basta con implementar la interfaz IPrinter para que se cumpla con el LSP.
                                :white_check_mark:
        

Pregunta 11
    
    Sea el siguiente fragmento de código, en el que la variable user es declarada usando un tipo implícito con la palabra clave var:
    var user = new User();
    ¿De qué tipo explícito podría ser declarada la variable local user? Más de una opción puede ser correcta.
    
    Seleccione una o más de una:

    a. User                             :white_check_mark:

    b. Un subtipo de User               :x:

    c. Un sucesor de User               :x:

    d. Un ancestro de User              :white_check_mark:

    e. Un supertipo de User             :white_check_mark:
    

Pregunta 12

    ¿Qué dice el principio de sustitución de Liskov?

    Seleccione una:

    a. El código que envia mensajes a un objeto del tipo S debe funcionar igual cuando ese objeto es subtipo T del tipo S
                                                                    :white_check_mark:
    b. Todas son correctas
                                                                    :x:
    c. El código que envia mensajes a un objeto de tipo T debe funcionar igual cuando ese objeto es supertipo S del tipo T
                                                                    :x:
    d. El código que envía mensajes a un objeto del tipo T tiene que ejecutar, pudiendo tener efectos colaterales, cuando ese objeto es subtipo S del tipo T
                                                                    :x:

Pregunta 13

    ¿Existe algún caso que operaciones polimórficas no cumplan con LSP?

    Seleccione una:
        Verdadero           :white_check_mark:

        Falso               :x:
   

Pregunta 14

    La siguiente interfaz:

    public interface IVehiculo

    {

        void Despegar();

        void EncenderMotor();

        void Frenar();

    }

        es implementada por las clases Auto y Helicóptero ya que ambos son vehículos.

        Sin embargo, en este diseño, el principio SRP       :x:                     no se cumple.
                                                ICP       :white_check_mark:



Pregunta 15

    El tipo Dictionary<T,K> es un tipo Genérico     :white_check_mark:

    Dictionary<string,Button> es un tipo   Parámetro  :x:
                                           Construido :white_check_mark:

    y en ese tipo Button es un tipo Construido   :x:
                                    Parametro    :white_check_mark:



Pregunta 16

    Sea el siguiente código:

    public abstract class SalesBaseItem
    {
        public abstract double SubTotal { get; }
        public abstract string GetTextToPrint();
    }

    public class SalesLineItem : SalesBaseItem
    {
        public SalesLineItem(double quantity, ProductSpecification product)
        {
            this.Quantity = quantity;
            this.Product = product;
        }
        ...
    }

    public class SaleDiscount : SalesBaseItem
    {
        public SaleDiscount(double ammount)
        {
            this.Ammount = ammount;
        }
        ...
    }

    public class Sale
    {
        private List<SalesLineItem> lineItems = new List<SalesLineItem>();
        ...
        public SalesLineItem AddLineItem(double quantity, ProductSpecification product)
        {
            SalesLineItem item = new SalesLineItem(quantity, product);
            this.lineItems.Add(item);
            return item;
        }
    }

        ¿Se puede decir que está bien implementado el OCP? Los puntos suspensivos son para obviar el resto de la implementación de la clase

        a. Está bien aplicado porque puedo agregar más tipos de sales siempre y cuando hereden de SalesBaseItem
                                                                                                            :x:
        b. No está bien aplicado ya que en la clase Sale sigo teniendo instancias de SalesLineItem
                                                                                                            :white_check_mark:
        c. No está bien aplicado porque si quiero agregar una responsabilidad nueva tengo que modificar las clases
                                                                                                            :x:

Pregunta 17

    Sea una clase Sale que contiene instancias de SalesLineItem:

    public class Sale
    {
        private List<SalesLineItem> lineItems = new List<SalesLineItem>();
        ...
    } 


    Seleccione una:

    a.
    Esta implementación es mejor según Creator porque permite a cualquier objeto crear instancias de SalesLineItem:

    public void AddLineItem(SalesLineItem item)
    {
        this.lineItems.Add(item);
    }
                            :x:
    b.
    Esta implementación es mejor según Creator porque Sale tiene una relación de agregación con instancias de SalesLineItem:

    public void AddLineItem(double quantity, ProductSpecification product)
    {
        SalesLineItem item = new SalesLineItem(quantity, product);
        this.lineItems.Add(item);
    }
                            :white_check_mark:


Pregunta 18

    Sea el siguiente fragmento de un programa:

    public class Page
    {
        Action post;
        public Page(string actionName, Uri actionUri)
        {
            this.post = new Action(actionName, actionUri)
            ...   
        }
        ...
    }

        Seleccione una:

        a.
        Creator no está bien aplicado. Como Page no tiene toda la información necesaria para crear instancias de Action no debería hacerlo; en su lugar debería recibir instancias ya creadas:

        public class Page
        {
            Action post;
            public Page(Action post)
            {
                this.post = post;
                ...   
            }
            ...
        }
                            :white_check_mark:
        b.
        Creator está aplicado correctamente. Como Page usa instancias de Action, está bien que las cree con la información que recibe como argumento

        Retroalimentación
        Respuesta incorrecta.
        La respuesta correcta es: Creator no está bien aplicado. Como Page no tiene toda la información necesaria para crear instancias de Action no debería hacerlo; en su lugar debería recibir instancias ya creadas:
        public class Page
        {
            Action post;
            public Page(Action post)
            {
                this.post = post;
                ...   
            }
            ...
        }
                            :x: