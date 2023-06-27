# Glosario de php



php cuenta con un servidor temporal el cual se puede  ejecutar con el siguiente comando:

```bash
php -S localhost:3000
```

con  el parámetro -S  podemos indicarle que ejecute un servidor de localhost en el puerto 3000.



### Funciones de salida en php

**echo** :

```php
echo "texto a imprimir"
```

echo es una de las funciones para imprimir en php. se utiliza para mostrar una o varias cadenas de texto en la salida al servidor. 

**printf**

```php
$texto = "Mudo";
printf("Hola %s",$texto);
```

esta función solo puede imprimir una cadena de texto a la vez



#### Variables y constantes

##### variables

las variables en PHP se definen usando el símbolo $ seguido del nombre de la variable. ejemplo

```php
$miVariable = "esta es mi variable";
```



##### constantes

las constantes PHP a igual que en cualquier lenguaje de programación son espacios reservados en
memoria que no cambian durante la ejecución de un programa. ejemplo 

```php
// definimos la constante PI
define("PI",3.1416);
```



### Tipos de datos en php

en php existen varios tipos de datos. los mas comunes son:

- Enteros (int) : numeros sin decimales

- Punto flotante (float): numeros con decimales
- Cadenas de texto (String): texto o caracteres
- Booleanos (bool) : true | false
- Arreglos (array):  [ ] colecciones de datos
- Objetos (object):  usado para almacenar instancias de clases
- Recursos (resource) : referencias a recursos externos
- Nulos (null):  usado para representar datos sin val$miArrayor



### Arreglos, Arreglos asociativos y funciones para arreglos

Los arreglos en PHP son estructuras de datos que permiten almacenar múltiples valores en una sola
variable. Los arreglos en PHP pueden ser indexados numéricamente o
asociativamente.

ejemplos 

```php
// aray indexado numericamente
$miArray = ["valor1",'valor2'];
$miArray = array("valor1","valor2");

// array asociativos 
$myArrayKv = [
 'clave' => 'valor'   
];

$myArrayKv = array(
	'clave' =>'valor'
); 


// para imprimir un dato de un array asociativo se puede hacer asi: 
echo $myArrayKv['clave']; //resultado: 'valor'
```





### Isset  y  Empty

La función isset() comprueba si una variable o un elemento de un array está definido y no es null.
Esta función devuelve true si la variable o el elemento de array existe y tiene un valor, y false en caso
contrario

```php
$miVar = "hola";
if(isset($miVar)){
    echo "variable esta definida y tiene valor";
}else{
    echo "la variable no esta definida o no tiene valor";
}
```



la función empty() comprueba si una variable o un elemento de un array está vacío.
Esta función devuelve true si la variable o el elemento de array no tiene un valor definido, o si tiene
un valor que se considera vacío (por ejemplo, una cadena vacía, 0, false, null, un array vacío, entre
otros), y false en caso contrario.

```php
$miVar = "hola";
if(empty($miVar)){
    echo "variable esta vacia o no definida";
}else{
    echo "la variable tiene valor";
}
```

### 



### Métodos útiles en arrays

```php
// in_array - busca un elemento en un array
in_array('elemento',$miArray);


// ordenar elementos de un array
$nums = [1,2,3,4];
sort($nums);  //de menor a mayor
rsort($nums); //de mayor a menor


// ordenar elemenos de una array asociativo 

$miArray = [
    'nombre' => 'Andres',
    'Edad' => 22
]

asort($miArray);   // ordena por valores  (alfabetico)
arsort($miArray);   // ordena por valores   (Z primero)

ksort($miArray);    // ordena por keys (alfabetico)
ksort($miArray);    // ordena por keys (Z - A) 


```

y muchos otros métodos que nos ofrece php , se recomienda revisar documentación oficial de php 

### Funciones mas usadas para la manipulación de data

array_flip(): Intercambia las claves con sus valores correspondientes en un array.
array_fill(): Rellena un array con un valor especificado.
array_filter(): Filtra los elementos de un array utilizando una función de devolución de llamada.
array_map(): Aplica una función a cada elemento de un array y devuelve un nuevo array con los
resultados.
array_reduce(): Reduce un array a un solo valor aplicando una función de devolución de llamada.
array_key_exists(): Comprueba si una clave existe en un array.
in_array(): Comprueba si un valor existe en un array.
array_rand(): Devuelve una o varias claves aleatorias de un array.

array_unique(): Elimina los valores duplicados de un array.
array_intersect(): Devuelve un array con los valores comunes a todos los arrays dados.
array_diff(): Devuelve un array con los valores del primer array que no están presentes en los arrays
adicionales.
array_push(): Agrega uno o más elementos al final de un array.
array_pop(): Extrae y elimina el último elemento de un array.
array_reverse(): Revierte el orden de los elementos en un array.
array_sum(): Devuelve la suma de todos los valores de un array numérico.

en:  https://www.php.net/download-docs.php



### Estructuras de control

Las estructuras de control en programación son herramientas que se utilizan para controlar el flujo
de ejecución de un programa.

- Estructuras de control condicionales: 

  - ```php
    if (condicion){
        // acciones si se cumple 
    }else{
        // acciones si no se cumple
    }
    ```

  - ```php
    $variable = 'a'; 
    switch ($variable) {
        case 'a':
            # acciones si el caso de la variable es a
            break;
        case 'b':
            # acciones si el caso de la variable es b
            break;
        default:
            # acciones default
            break;
    }
    ```

- Estructuras de control de repetición: también conocidas como bucles o ciclos.

  - ```php
    // bucle for
    
    for ($i=0; $i < 2 ; $i++) { 
        echo "hola";
    }
    
    
    //bucle foreach     comunmente usadas para array asociativos
    foreach ($variable as $key => $value) {
        echo "llave: $key \nvalor: $value";
    }
    
    foreach ($variable as $element) {
        echo "elemento: $element";
    }
    
    
    // bucle while 
    
    while (condicion) {
        // acciones a realizar mientras la condicion se cumpla
    }
    
    
    // bucle do while
    do {
        // acciones que se realizan almenos una ve
    } while (condicion)  // si la condicion se cumple , se realizaran otra vez
        
     
    ```

- Estructuras de control de excepciones: permiten manejar errores o situaciones inesperadas
  que puedan ocurrir durante la ejecución del programa.

  - ```php
    
        try {
            //code...     aqui se intenta realizar la tarea y si falla , en el cath se 			captura el error
        } catch (\Throwable $th) {
            //throw $th;      aqui se captura la excepción 
        }
    ```

​	



### Funciones en php

las funciones definidas por el usuario son bloques de código que se pueden llamar
y ejecutar en cualquier parte de un programa para realizar una tarea específica.

definición de funciones: 

```php
// asi se puede definir una funcion en php
function FunctionName(/*parametros*/){
    // operaciones a realizar
    
    return /*lo que retorna*/;
}

// funciones que no retornan valores , pero realizan operaciones

function sumar(int $n1 + int $n2):void {
    echo $n1+$n2;
}
sumar();
```





### Requerir o incluir archivos

En PHP, include, require, include_once y require_once son funciones que se utilizan para incluir
archivos externos en un programa.

es como la forma de usar módulos o funcionalidades hechas en otros archivos.

```php
/*
	include y include_once permiten incluir un archivo PHP en el programa. 
	La diferencia	entre ellas es que:
    include puede incluir el mismo archivo varias veces 
    mientras que include_once asegura que el archivo solo se incluya una vez en el 			programa.
*/
include "ruta/del/archivo.php";
include_once "ruta/del/archivo.php";



/*
	require y require_once son similares a include y include_once, pero en caso de que el     archivo no pueda ser encontrado, se detendrá la ejecución del programa. 
	Al utilizar require_once, se asegura que el archivo solo se incluya una vez en el 		programa.
*/
require "ruta/del/archivo.php";
require_once "ruta/del/archivo.php";
```



### Json_encode y Json_decode

La función json_encode() en PHP se utiliza para convertir una estructura de datos en PHP en una
cadena JSON.

```php
$datos = [
    "nombre" => "Juan",
    "edad" => 25,
    "email" => "juan@example.com"
];

echo json_encode($datos); // convierte la salida en una estructura json
```



La función json_decode() en PHP se utiliza para convertir una cadena JSON en una estructura de
datos de PHP.



```php
// estructura json
$json ='{ "nombre": "Juan", "edad": 25, "email": "juan@example.com"}';

$datosPhp = json_decode($json,true); // el parametro true , indica que quiero que esos 											datos sean un array asociativo
```





# Programación Orientada a Objetos (POO)

En la programación orientada a objetos, los objetos son la base fundamental y se crean a partir de
clases. Una clase es una plantilla o un molde que define las propiedades y comportamientos que
tendrán los objetos que se creen a partir de ella.

Los principales conceptos de la programación orientada a objetos son:

- **Clase**: Es una plantilla o definición que describe las características y comportamientos de los
  objetos que se pueden crear a partir de ella.

- **Objeto**: Es una instancia de una clase. Representa un individuo o entidad específica y tiene
  sus propias propiedades y comportamientos.

- **Atributos**: Son las propiedades o características de un objeto. Definen el estado de un objeto
  y se representan mediante variables en la clase

- **Métodos**: Son las acciones o comportamientos que un objeto puede realizar. Representan las
  operaciones que pueden realizarse con un objeto y se definen como funciones en la clase.

- **Encapsulamiento**: Es el principio que establece que los atributos y métodos relacionados deben
  agruparse en una clase para ocultar los detalles internos y exponer solo una interfaz pública.
  Esto se logra mediante la especificación de niveles de acceso (público, privado, protegido)
  para los atributos y métodos.
- **Herencia**: Es un mecanismo que permite crear nuevas clases basadas en clases existentes. La
  clase que se utiliza como base se denomina "clase padre" o "superclase", y la clase que se
  deriva se llama "clase hija" o "subclase". La herencia permite la re-utilización de código y la
  creación de jerarquías de clases

- **Polimorfismo**: Es la capacidad de un objeto de tomar diferentes formas o comportarse de
  diferentes maneras según el contexto. Permite utilizar una interfaz común para objetos de
  diferentes clases y proporciona flexibilidad y extensibilidad en el diseño de programas.

La programación orientada a objetos permite organizar y modularizar el código de manera más clara
y estructurada, lo que facilita el desarrollo, la mantenibilidad y la reutilización del código. Es
ampliamente utilizado en diversos lenguajes de programación, como Java, C++, Python, PHP, entre
otros.





## Modificadores de acceso en PHP (encapsulamiento)

Los modificadores de acceso son palabras clave utilizadas en la programación orientada a objetos
para controlar la visibilidad y el acceso a los miembros (atributos y métodos) de una clase. Estos
modificadores permiten establecer qué partes del código pueden acceder y modificar dichos
miembros.
En PHP, hay tres modificadores de acceso para controlar la visibilidad de propiedades y métodos en
una clase:

- **public**: Los miembros declarados como public son accesibles desde cualquier lugar, ya sea
  desde dentro de la clase, desde las clases heredadas o desde fuera de la clase. Son visibles
  para todos.

- **private**: Los miembros declarados como private solo son accesibles desde dentro de la
  misma clase en la que se definen. No pueden ser accedidos desde fuera de la clase, ni
  siquiera por las clases heredadas.

- **protected**: Los miembros declarados como protected son accesibles desde dentro de la
  misma clase y desde las clases heredadas (subclases). Sin embargo, no pueden ser accedidos
  desde fuera de la clase directamente.



## Clases

En programación orientada a objetos (POO), una clase es una plantilla o molde para crear objetos. Define un conjunto de atributos y métodos que caracterizan a los objetos que se pueden crear a partir de ella. La clase actúa como un plano o descripción de cómo debe ser un objeto, y los objetos son las instancias concretas de esa clase.

En la definición de una clase, se especifican los atributos (propiedades o variables) que tiene el objeto y los métodos (funciones) que puede realizar. Los atributos representan el estado o las características del objeto, mientras que los métodos definen su comportamiento o las acciones que puede realizar.

```php
class Persona {
    // Atributos
    private $nombre; //atributos encapsulados como privados
    public $edad; // atributos encapsulados como publicos
    protected $cedula //atributos encapsulados como protegidos
    
    // Métodos
    public function saludar() {
        echo "Hola, soy " . $this->nombre . " y tengo " . $this->edad . " años. y esta es 				mi cedula: ". $this->cedula;
    }
}
```



## Métodos estaticos

En PHP, los métodos estáticos son métodos de una clase que se pueden llamar sin crear una instancia de la clase. A diferencia de los métodos de instancia, los métodos estáticos pertenecen a la clase en sí misma en lugar de a objetos individuales. Se pueden acceder directamente desde la clase utilizando el operador de resolución de ámbito `::`.

Los métodos estáticos se definen con la palabra clave `static` antes del nombre del método. No pueden acceder a los atributos de instancia de la clase porque no están asociados a objetos individuales, pero sí pueden acceder a otros métodos estáticos y a los atributos estáticos de la clase.

```php
class MathUtils {
    public static function sumar($a, $b) {
        return $a + $b;
    }
}

$resultado = MathUtils::sumar(3, 5);
echo $resultado;  // Imprime 8
```

En este ejemplo, la clase `MathUtils` tiene un método estático `sumar()` que toma dos números como argumentos y devuelve su suma. No es necesario crear una instancia de la clase `MathUtils` para llamar al método `sumar()`. Se puede acceder directamente a través de la clase utilizando `MathUtils::sumar()`.





## Herencia 

Herencia
La herencia en programación es un concepto que permite crear nuevas clases basadas en clases
existentes, aprovechando y extendiendo su funcionalidad. La clase existente se conoce como clase
base o clase padre, mientras que la nueva clase creada se llama clase derivada o clase hija.

```php
class Animal {
    protected $nombre;
    
    public function __construct($nombre) {
        $this->nombre = $nombre;
    }
    
    public function hacerSonido() {
        echo "El animal hace un sonido.";
    }
}

class Perro extends Animal {   // extendemos o heredamos los atributos y metodos Animal
    public function hacerSonido() {
        echo "El perro ladra.";
    }
    
    public function saludar() {
        echo "¡Hola! Soy un perro llamado " . $this->nombre . ".";
    }
}
	
// nuestra instancia de la clase hija podra usar los atributos o metodos de clase padre
// o usar los suyos propios

$perro = new Perro("Bobby");
$perro->hacerSonido();  // Imprime "El perro ladra."
$perro->saludar();  // Imprime "¡Hola! Soy un perro llamado Bobby."
```



## Clases abstractas

 una clase abstracta es una clase que no se puede instanciar directamente, sino que se utiliza como una clase base para otras clases. Una clase abstracta define la estructura y el comportamiento común que deben tener las clases derivadas, pero no puede ser instanciada por sí misma. Se utiliza para establecer una interfaz común y proporcionar cierta implementación básica que se espera que las clases derivadas completen o modifiquen.

```php
abstract class Figura {
    protected $color;
    
    public function __construct($color) {
        $this->color = $color;
    }
    
    abstract public function calcularArea();
    
    public function getColor() {
        return $this->color;
    }
}
```



En este ejemplo, la clase `Figura` es una clase abstracta que define una propiedad `$color` y tres métodos: `__construct()` para inicializar el color, `calcularArea()` que es un método abstracto sin implementación y `getColor()` para obtener el color de la figura.

Una clase abstracta puede tener métodos abstractos y métodos concretos. Los métodos abstractos se definen sin implementación, simplemente declarando su firma y terminando con un punto y coma (;). Estos métodos deben ser implementados por las clases derivadas que heredan de la clase abstracta.

Las clases que heredan de una clase abstracta deben implementar todos los métodos abstractos de la clase base o también pueden ser declaradas como clases abstractas.

```php
class Rectangulo extends Figura {
    private $largo;
    private $ancho;
    
    public function __construct($color, $largo, $ancho) {
        parent::__construct($color); // intanciamos el constructor de la clase padre
        $this->largo = $largo;
        $this->ancho = $ancho;
    }
    
    public function calcularArea() {
        return $this->largo * $this->ancho;
    }
}

$rectangulo = new Rectangulo("rojo", 5, 3);
echo $rectangulo->calcularArea();  // Imprime 15
echo $rectangulo->getColor();  // Imprime "rojo"
```



En este ejemplo, la clase `Rectangulo` hereda de la clase abstracta `Figura` y proporciona una implementación concreta del método abstracto `calcularArea()`. También define sus propios atributos `$largo` y `$ancho`. Al crear un objeto de la clase `Rectangulo` y llamar al método `calcularArea()` o `getColor()`, se utiliza la implementación definida en la clase `Rectangulo`.

Las clases abstractas en PHP son útiles cuando se desea proporcionar una estructura común y establecer una interfaz que las clases derivadas deben seguir. Esto promueve la coherencia y la reutilización de código al tiempo que permite la especialización y personalización en las clases derivadas.



## Interfaces

una interfaz es una estructura que define un conjunto de métodos que deben ser implementados por cualquier clase que la utilice. Una interfaz define un contrato o una especificación que las clases deben cumplir, sin preocuparse por la implementación concreta. Las interfaces permiten la implementación de la herencia múltiple en PHP, ya que una clase puede implementar varias interfaces.

Para definir una interfaz en PHP, se utiliza la palabra clave `interface`. Aquí tienes un ejemplo básico de cómo se define una interfaz en PHP:

```php
interface Animal {    // dificionn de  una interface
    public function hacerSonido();
    public function moverse();
}
```

En este ejemplo, la interfaz `Animal` define dos métodos: `hacerSonido()` y `moverse()`. Cualquier clase que implemente la interfaz `Animal` debe proporcionar una implementación de estos dos métodos.

para decirle a una clase que utilice una interface lo hacemos por medio de la palabra implements:

```php
class Perro implements Animal {    // asi le indicamos que implemente la interfaz
    public function hacerSonido() {
        echo "El perro ladra.";
    }
    
    public function moverse() {
        echo "El perro se mueve corriendo.";
    }
}

$perro = new Perro();
$perro->hacerSonido();  // Imprime "El perro ladra."
$perro->moverse();  // Imprime "El perro se mueve corriendo."
```

En este ejemplo, la clase `Perro` implementa la interfaz `Animal` y proporciona una implementación para los métodos `hacerSonido()` y `moverse()`. Al crear un objeto de la clase `Perro` y llamar a los métodos definidos en la interfaz, se utiliza la implementación proporcionada en la clase `Perro`.

Las interfaces en PHP permiten establecer contratos entre las clases y asegurar que las clases implementen ciertos métodos. Esto facilita la interoperabilidad y el intercambio de implementaciones entre diferentes clases. Las interfaces son especialmente útiles cuando se desea definir un conjunto de métodos comunes que deben ser implementados por varias clases, sin especificar la lógica concreta de cada método.



## Composer 

Composer es una herramienta de administración de dependencias para PHP. Se utiliza para gestionar las bibliotecas y paquetes de terceros que son necesarios en un proyecto PHP. Composer simplifica el proceso de instalación, actualización y carga de las dependencias de un proyecto, facilitando así el desarrollo y la gestión de las dependencias de software.

```json
{
    "name": "mi-proyecto",
    "description": "Descripción del proyecto",
    "type": "project",
    "require": {
        "php": "^7.4",
        "monolog/monolog": "^2.0"
    },
    "autoload": {
        "psr-4": {
            "MiProyecto\\": "src/"
        }
    }
}

```

la anterior es la estructura basica de un archivo composer.json



## SQL Structured Query Language

SQL (Structured Query Language) es un lenguaje de programación utilizado para administrar y
manipular bases de datos relacionales. Fue desarrollado en la década de 1970 y se ha convertido en
el estándar de facto para trabajar con bases de datos.
SQL permite a los usuarios crear, modificar y eliminar bases de datos, así como realizar consultas
para recuperar información específica de una base de datos. Con SQL, puedes crear tablas para
almacenar datos, definir relaciones entre las tablas, agregar, actualizar o eliminar registros y realizar
consultas complejas para obtener información precisa.



El lenguaje SQL consta de varios comandos, entre los que se incluyen:

- **DDL (Data Definition Language)**: Utilizado para definir y modificar la estructura de la base de
  datos. Incluye comandos como CREATE, ALTER y DROP para crear, modificar y eliminar tablas,
  índices, vistas, etc.

- **DML (Data Manipulation Language):** Utilizado para manipular los datos almacenados en la
  base de datos. Incluye comandos como INSERT, UPDATE y DELETE para agregar, actualizar y
  eliminar registros.

- **DQL (Data Query Language):** Utilizado para realizar consultas y recuperar información de la
  base de datos. El comando más común es SELECT, que permite especificar los criterios de
  búsqueda y los campos a recuperar.

- **DCL (Data Control Language):** Utilizado para controlar los privilegios de acceso a la base de
  datos. Incluye comandos como GRANT y REVOKE para otorgar y revocar permisos.





## API REST

Un API (Application Programming Interface, por sus siglas en inglés) es un conjunto de reglas y
protocolos que permite la comunicación entre distintos sistemas informáticos. En términos simples,
es una interfaz que define cómo los diferentes componentes de software deben interactuar entre sí.
Un API proporciona una forma estandarizada y estructurada para que las aplicaciones y servicios se
comuniquen y compartan datos y funcionalidades. A través de un API, una aplicación puede solicitar
información o realizar acciones en otra aplicación o servicio, sin necesidad de conocer los detalles
internos de cómo se implementa dicha funcionalidad.
Existen diferentes tipos de API, como las API web, que permiten la comunicación entre aplicaciones a
través de Internet utilizando protocolos como HTTP. También existen las API de sistema operativo,
que proporcionan acceso a las funciones y recursos del sistema operativo subyacente, y las API de
biblioteca, que ofrecen funciones y servicios específicos a los desarrolladores.
Las API han sido fundamentales en el desarrollo de aplicaciones modernas, ya que permiten la
integración de diferentes sistemas, el intercambio de datos y la creación de servicios y aplicaciones
más complejas a través de la reutilización de componentes existentes. También son ampliamente
utilizadas en el desarrollo de interfaces de programación para servicios web (API web) y aplicaciones
móviles, permitiendo la interacción con plataformas populares y servicios en la nube.



### Metodos HTTP

Los métodos HTTP son verbos o acciones que se utilizan en las solicitudes y respuestas de comunicación entre clientes y servidores en el protocolo HTTP (Hypertext Transfer Protocol). Cada método tiene un propósito específico y define la acción que debe realizar el servidor en respuesta a la solicitud del cliente. Aquí tienes una breve descripción de los métodos HTTP más comunes:

1. **GET**: El método GET se utiliza para solicitar y recuperar recursos del servidor. Se envía una solicitud al servidor para obtener información y el servidor responde con los datos solicitados. Este método no debe tener un efecto secundario y no debe modificar los datos en el servidor.
2. **POST**: El método POST se utiliza para enviar datos al servidor para su procesamiento. Es comúnmente utilizado para enviar formularios HTML o enviar datos al crear nuevos recursos en el servidor. Los datos se incluyen en el cuerpo de la solicitud y el servidor procesa la información enviada.
3. **PUT**: El método PUT se utiliza para enviar datos al servidor para crear o reemplazar un recurso completo en una ubicación específica. El cliente envía los datos en el cuerpo de la solicitud y el servidor actualiza o crea el recurso en la ubicación indicada.
4. **PATCH:** El método PATCH se utiliza para enviar datos al servidor para realizar una actualización parcial de un recurso. A diferencia de PUT, PATCH actualiza solo las partes especificadas del recurso en lugar de reemplazarlo por completo.
5. **DELETE:** El método DELETE se utiliza para solicitar al servidor que elimine un recurso específico. El cliente envía una solicitud de eliminación al servidor y, si se permite y es exitosa, el servidor elimina el recurso indicado.



### Response status

En el protocolo HTTP (Hypertext Transfer Protocol), el código de estado de respuesta HTTP indica el estado de la solicitud realizada por el cliente al servidor. El código de estado de respuesta se envía como parte de la respuesta del servidor y proporciona información sobre si la solicitud fue exitosa, redirigida, encontró un error, o si se requiere alguna acción adicional.

Los códigos de estado de respuesta HTTP están divididos en diferentes categorías:

1. **Códigos de estado informativos (1xx):** Indican que la solicitud ha sido recibida y el servidor continúa procesándola.
2. **Códigos de estado exitosos (2xx):** Indican que la solicitud ha sido recibida, entendida y aceptada correctamente por el servidor.
3. **Códigos de estado de redirección (3xx):** Indican que se requiere una acción adicional por parte del cliente para completar la solicitud.
4. **Códigos de estado de error del cliente (4xx):** Indican que ha ocurrido un error en la solicitud realizada por el cliente, como una solicitud incorrecta o recursos no encontrados.
5. **Códigos de estado de error del servidor (5xx):** Indican que ha ocurrido un error en el servidor al procesar la solicitud.

Algunos ejemplos comunes de códigos de estado de respuesta HTTP son:

- **200 OK:** Indica que la solicitud ha sido exitosa y se ha devuelto una respuesta satisfactoria.
- **301 Moved Permanently**: Indica que el recurso solicitado ha sido movido permanentemente a otra ubicación. El cliente debe actualizar su URL para futuras solicitudes.
- **404 Not Found:** Indica que el recurso solicitado no ha sido encontrado en el servidor.
- **500 Internal Server Error:** Indica que ha ocurrido un error interno en el servidor al procesar la solicitud.

Los códigos de estado de respuesta HTTP son importantes para los clientes y servidores, ya que proporcionan información sobre el resultado de la solicitud y ayudan a realizar acciones adecuadas en función del estado devuelto. Los clientes pueden interpretar los códigos de estado para mostrar mensajes de error relevantes o tomar acciones específicas, mientras que los servidores utilizan los códigos de estado para comunicar el resultado de la solicitud al cliente de manera estandarizada.



### Tipos de Autenticacion 

3.6.3. Tipos de autenticación
En API REST, existen varios métodos de autenticación que se utilizan para garantizar la seguridad y
proteger los recursos. Aquí tienes algunos ejemplos comunes de tipos de autenticación en API REST:


- **Autenticación basada en token (Token-Based Authentication)**: En este enfoque, el cliente
  envía un token de acceso con cada solicitud al servidor. El token es emitido por el servidor
  después de que el cliente proporciona sus credenciales de autenticación (como nombre de
  usuario y contraseña) de manera segura. El servidor verifica la validez del token antes de
  procesar la solicitud. Ejemplos de implementaciones populares de este tipo de autenticación
  son JSON Web Tokens (JWT) y OAuth 2.0.
- **Autenticación básica (Basic Authentication):** En este método, el cliente envía las credenciales
  (nombre de usuario y contraseña) codificadas en Base64 en el encabezado de la solicitud.
  Aunque es fácil de implementar, la autenticación básica no cifra las credenciales y, por lo
  tanto, no se considera segura para entornos no HTTPS.
- **Autenticación mediante API key (API Key Authentication):** En este enfoque, el cliente envía
  una clave de API junto con la solicitud al servidor. La clave de API es un identificador único y
  secreto que se emite al cliente para autenticarse en cada solicitud. El servidor verifica la
  validez de la clave de API antes de procesar la solicitud.
- **Autenticación mediante OAuth**: OAuth es un protocolo de autorización que permite a una
  aplicación solicitar acceso a los recursos protegidos en nombre de un usuario. El cliente
  obtiene un token de acceso válido después de que el usuario autoriza la aplicación. Este token
  se utiliza posteriormente para autenticar las solicitudes al servidor.
