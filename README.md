TECNOLÓGICO NACIONAL DE MÉXICO
INSTITUTO TECNOLÓGICO DE TLÁHUAC 
“LA ESENCIA DE LA GRANDEZA RADICA EN LAS RAICES”
INGENIERIA EN SISTEMA COMPUTACIONALES


El Modelo-Vista-Controlador (MVC)

DOCENTE: 
Cordeo Ocampo Martin Ramon
ESTUDIANTE: 
Ortiz Molina Ameyalli 
Hernandez Ramirez Paola Michelle
MATERIA: PROG. PHP CON MVC
 GRUPO: 8S2



Índice
Resumen	3
Introducción	4
Descripción Técnica de la Aplicación Web	5
Organización de Carpetas y Archivos	5
La estructura de archivos de la aplicación sigue la convención del patrón MVC	5
Diagramas Técnicos	5
•	Diagrama de Clases	5
•	Diagrama Entidad-Relación (ER)	6
Fragmentos Descriptivos de Código:	6
Modelo (modelo.php)	6
Vista (perfil.php)	7
Controlador (usuarioController.php)	8
Conclusión.	10
Referencias.	11





Resumen

El Modelo-Vista-Controlador (MVC) ha sido reconocido como uno de los patrones arquitectónicos más fundamentales y efectivos en el desarrollo de aplicaciones web. Este enfoque se ha convertido en un estándar en la industria debido a su capacidad para ofrecer una estructura clara y organizada que promueve la separación de responsabilidades y facilita el desarrollo, mantenimiento y escalabilidad de proyectos web.
En el contexto de MVC, se dividen las preocupaciones de una aplicación web en tres componentes distintos: el Modelo, la Vista y el Controlador. Cada uno de estos componentes desempeña un papel específico y se comunica entre sí para lograr el funcionamiento completo de la aplicación. El Modelo se encarga de gestionar los datos y la lógica de negocio, la Vista se encarga de la presentación de los datos al usuario, y el Controlador maneja las solicitudes del usuario y coordina la interacción entre el Modelo y la Vista.
La implementación del patrón MVC implica una estructura organizada de archivos y carpetas que refleja la separación de responsabilidades entre los componentes. Por lo general, se encuentran tres carpetas principales: Modelo, Vista y Controlador. En la carpeta Modelo se alojan las clases y funciones que gestionan los datos y la lógica de negocio. La carpeta Vista contiene los archivos de plantillas HTML con incrustaciones de código PHP para la presentación de la interfaz de usuario. Mientras que la carpeta Controlador alberga los archivos que manejan las solicitudes del usuario y coordinan la interacción entre el Modelo y la Vista.
Además de la organización de archivos, la integración de elementos como archivos "assets" y un archivo index.php es esencial para una aplicación web completa. Los archivos "assets" contienen recursos estáticos como hojas de estilo CSS, scripts JavaScript e imágenes, que son utilizados por la Vista para mejorar la apariencia y la funcionalidad de la aplicación. Por otro lado, el archivo index.php actúa como el punto de entrada principal de la aplicación, dirigiendo las solicitudes del usuario al Controlador correspondiente y dando inicio al flujo de la aplicación.
Por último, la inclusión de diagramas técnicos como diagramas de clases o diagramas entidad-relación enriquece nuestra comprensión de la arquitectura de la aplicación y las relaciones entre sus componentes. Estas representaciones visuales son herramientas valiosas que ayudan a planificar, diseñar y comunicar eficazmente la estructura y el flujo de la aplicación.



Introducción
El Modelo-Vista-Controlador (MVC) ha sido reconocido como uno de los patrones arquitectónicos más efectivos y ampliamente adoptados en el desarrollo de aplicaciones web. Su popularidad se debe a su capacidad para proporcionar una estructura clara y modular que promueve la separación de responsabilidades, facilitando así el desarrollo, mantenimiento y escalabilidad de proyectos web de cualquier tamaño y complejidad.
En el ecosistema digital actual, donde la demanda de aplicaciones web robustas y dinámicas sigue en aumento, la adopción de patrones arquitectónicos como MVC se ha vuelto imperativa para los desarrolladores y equipos de desarrollo. La necesidad de construir sistemas que no solo sean funcionales, sino también flexibles y fáciles de mantener a largo plazo, ha llevado a una mayor valoración de los principios de diseño como los que se encuentran en el MVC.
Al sumergirnos en la implementación del patrón MVC, nos encontramos con una estructura bien definida que consta de tres componentes principales: el Modelo, que gestiona los datos y la lógica de negocio; la Vista, que se encarga de la presentación de la interfaz de usuario; y el Controlador, que actúa como intermediario entre el Modelo y la Vista, controlando el flujo de la aplicación y procesando las interacciones del usuario. Una de las principales ventajas del patrón MVC es su capacidad para promover una separación clara de preocupaciones. Esta división permite a los desarrolladores trabajar de manera más eficiente en equipos, ya que cada componente puede ser desarrollado, probado y mantenido de forma independiente. Además, esta modularidad facilita la reutilización de código y la incorporación de nuevas características sin afectar otras partes del sistema, lo que resulta en un desarrollo más ágil y menos propenso a errores.
Al analizar la implementación práctica del MVC en una aplicación web, es esencial considerar la estructura de archivos y carpetas, así como la integración de elementos como archivos "assets" y el archivo index.php. Estos elementos desempeñan un papel crucial en la creación de una aplicación web completa y funcional, proporcionando los recursos necesarios para la presentación de la interfaz de usuario y estableciendo el punto de entrada principal para la aplicación.
Además, la inclusión de diagramas técnicos, como diagramas de clases o diagramas entidad-relación, enriquece nuestra comprensión de la arquitectura subyacente de la aplicación y las relaciones entre sus componentes. Estas representaciones visuales son herramientas valiosas que ayudan a los desarrolladores a planificar, diseñar y comunicar eficazmente la estructura y el flujo de la aplicación, lo que contribuye a un desarrollo más sólido y orientado a objetivos.
![modelo , vista controlador](https://raw.githubusercontent.com/amibi0108/amibi0108/fe3dd58d23194932ab1de57de3504ed4097419bb/mvc.jpg)

Descripción Técnica de la Aplicación Web
La aplicación web de ejemplo que utilizaremos es un sistema de gestión de perfiles de usuario. Permitirá a los usuarios registrarse, iniciar sesión, ver y editar su perfil. La aplicación está construida siguiendo el patrón MVC para garantizar una separación clara de responsabilidades y una fácil mantenibilidad.

Organización de Carpetas y Archivos

La estructura de archivos de la aplicación sigue la convención del patrón MVC

•	Modelo: Contiene clases PHP que gestionan los datos y la lógica de negocio. Por ejemplo, la clase Usuario maneja la información del usuario y las operaciones relacionadas con la base de datos.

•	Vista: Almacena archivos de plantillas HTML con incrustaciones de código PHP para la presentación de la interfaz de usuario. Por ejemplo, perfil.php muestra el perfil del usuario.

•	Controlador: Contiene archivos PHP que manejan las solicitudes del usuario y coordinan la interacción entre el Modelo y la Vista. Por ejemplo, usuarioController.php procesa las acciones relacionadas con el usuario, como el registro y la edición del perfil.

Assets: Aquí se encuentran recursos estáticos como archivos CSS, JavaScript e imágenes.

index.php: Es el archivo principal de la aplicación que actúa como punto de entrada. Dirige las solicitudes del usuario al controlador correspondiente.

Diagramas Técnicos
•	Diagrama de Clases Muestra las clases en el sistema y sus relaciones. Por ejemplo, la clase Usuario se relaciona con la clase Perfil mediante una asociación uno a uno.

![Diagrama UML](https://raw.githubusercontent.com/amibi0108/amibi0108/6026148c5e7f135ea95686355ce68ed806fe8611/diagrama%20de%20clases%20uml.jpg)


•	Diagrama Entidad-Relación (ER) Representa la estructura de la base de datos. Por ejemplo, la tabla usuarios tiene una relación uno a uno con la tabla perfiles.
![Diagrama entidad relacion ER](https://raw.githubusercontent.com/amibi0108/amibi0108/74a17a4b683df535de4b695735f1b7bd27b2d318/MOD%20E-R.png)

Fragmentos Descriptivos de Código:
Modelo (modelo.php)
class Usuario {
    	private $id;
   	 private $nombre;
    	private $email;
    		// Otros atributos y métodos

    public function __construct($nombre, $email) {
        	$this->nombre = $nombre;
        	$this->email = $email;
    						}
}


El código  define una clase llamada Usuario, que representa a un usuario en el contexto de una aplicación web u otro sistema. Aquí está la descripción de lo que hace este código:

•	private $id;, private $nombre;, private $email;: Estos son atributos de la clase Usuario. Son privados, lo que significa que solo pueden ser accedidos directamente desde dentro de la clase misma. $id representa el identificador único del usuario, $nombre representa el nombre del usuario y $email representa la dirección de correo electrónico del usuario.

•	public function __construct($nombre, $email) { ... }: Este es el constructor de la clase Usuario. Un constructor es un método especial que se llama automáticamente cuando se crea un nuevo objeto de la clase. Toma dos parámetros, $nombre y $email, que se utilizan para inicializar los atributos $nombre y $email del objeto. Dentro del constructor, $nombre y $email se asignan a los atributos correspondientes usando la sintaxis $this->nombre = $nombre; y $this->email = $email;.


•	En resumen, esta clase Usuario permite crear objetos que representan usuarios, con atributos como el nombre y el correo electrónico. El constructor se encarga de inicializar estos atributos cuando se crea un nuevo objeto Usuario.
Vista (perfil.php)

<html>
<head>
    <title>Perfil de Usuario</title>
    <link rel="stylesheet" href="assets/style.css">
</head>
<body>
    <h1>Perfil de Usuario</h1>
    <p>Nombre: <?php echo $usuario->nombre; ?></p>
    <p>Email: <?php echo $usuario->email; ?></p>
    <!-- Otros detalles del perfil -->
</body>
</html>
En el siguiente código HTML , es una plantilla de la vista para mostrar el perfil de un usuario en una aplicación web. 

•	<html>: Esta etiqueta indica el comienzo de un documento HTML.
•	<head>: Define la sección de encabezado del documento HTML, donde se incluyen metadatos y referencias a recursos externos como hojas de estilo y scripts.
•	<title>Perfil de Usuario</title>: Define el título del documento, que aparecerá en la pestaña del navegador o en la barra de título de la ventana.
•	<link rel="stylesheet" href="assets/style.css">: Esta línea enlaza la hoja de estilo CSS ubicada en la carpeta "assets/style.css" para aplicar estilos al contenido de la página. La etiqueta <link> se utiliza para vincular una hoja de estilo externa al documento HTML.
•	<body>: Define la sección del cuerpo del documento HTML, donde se coloca el contenido visible de la página.
•	<h1>Perfil de Usuario</h1>: Encabezado de nivel 1 que muestra el título "Perfil de Usuario".
•	<p>Nombre: <?php echo $usuario->nombre; ?></p>: Un párrafo que muestra el nombre del usuario. La etiqueta PHP <?php echo $usuario->nombre; ?> incrustada en HTML se utiliza para imprimir el nombre del usuario recuperado de la variable $usuario. Esto asume que la variable $usuario contiene un objeto con una propiedad nombre.
•	<p>Email: <?php echo $usuario->email; ?></p>: Otro párrafo que muestra el correo electrónico del usuario. Similar al párrafo anterior, imprime el correo electrónico del usuario recuperado de la variable $usuario.
•	<!-- Otros detalles del perfil -->: Esto es un comentario HTML que indica que aquí podrían incluirse otros detalles del perfil del usuario, pero actualmente no están presentes en la plantilla.
•	</body>: Marca el final del cuerpo del documento HTML.
•	</html>: Marca el final del documento HTML.


Controlador (usuarioController.php)

require_once 'modelo.php';
require_once 'vista.php';
// Procesamiento de la solicitud para ver el perfil del usuario
$usuario = obtenerUsuarioPorId($id);
include 'perfil.php';


Este fragmento de código PHP se encarga de procesar la solicitud para ver el perfil de un usuario en una aplicación web. Aquí está la descripción de lo que hace este código:

•	require_once 'modelo.php'; y require_once 'vista.php';: Estas líneas incluyen los archivos modelo.php y vista.php en el script PHP actual. La función require_once se utiliza para incluir un archivo PHP y garantiza que se incluya solo una vez, evitando la inclusión repetida de un mismo archivo.

•	$usuario = obtenerUsuarioPorId($id);: Esta línea llama a la función obtenerUsuarioPorId($id) para obtener los datos del usuario cuyo identificador ($id) se proporciona. Presumiblemente, esta función está definida en el archivo modelo.php y se encarga de recuperar los datos del usuario de alguna fuente de datos, como una base de datos. El resultado se almacena en la variable $usuario.

•	include 'perfil.php';: Esta línea incluye el archivo perfil.php en el script actual. El contenido de perfil.php probablemente sea una plantilla de vista que muestra el perfil del usuario. Al incluir este archivo, se renderiza la vista del perfil del usuario en la página web actual.
Este fragmento de código PHP carga el modelo de datos y la vista necesarios, procesa la solicitud para obtener los datos del perfil del usuario, y luego incluye la vista del perfil del usuario en la página web actual.

Conclusión.

La aplicación web descrita, diseñada bajo el sólido patrón arquitectónico Modelo-Vista-Controlador (MVC), ofrece un claro ejemplo de cómo se puede implementar una estructura robusta y escalable para sistemas web. La adopción de esta arquitectura garantiza una clara separación de responsabilidades entre las diferentes capas del sistema, facilitando un desarrollo más organizado y modularizado. La distinción entre el Modelo, la Vista y el Controlador no solo promueve una mejor comprensión del código, sino que también simplifica el proceso de mantenimiento y permite una expansión más sencilla del proyecto a medida que los requisitos evolucionan.

Una de las ventajas más destacadas del enfoque MVC es su capacidad para facilitar la reutilización de código. Al dividir la aplicación en componentes bien definidos, se crea un entorno propicio para la creación de módulos independientes y fácilmente intercambiables. Esto no solo agiliza el proceso de desarrollo, sino que también contribuye a la estandarización del código y la promoción de buenas prácticas de programación.

Además, la integración de diagramas técnicos, como los diagramas de clases y los diagramas entidad-relación, desempeña un papel crucial en la comprensión y la comunicación de la estructura subyacente de la aplicación. Estos diagramas actúan como una guía visual que ayuda a los desarrolladores a comprender mejor las relaciones entre los diferentes componentes del sistema, lo que facilita la identificación de posibles áreas de mejora y optimización.

La inclusión de archivos "assets", como hojas de estilo CSS, scripts JavaScript e imágenes, y el archivo index.php como punto de entrada principal, son elementos fundamentales para garantizar una experiencia de usuario completa y cohesiva. Los archivos "assets" permiten una presentación visual atractiva y una interacción dinámica en la interfaz de usuario, mientras que el archivo index.php proporciona una entrada clara y organizada al sistema.

En resumen, el uso del patrón MVC no solo es esencial para el desarrollo eficiente de aplicaciones web modernas, sino que también representa un enfoque sólido y probado para la creación de sistemas escalables y mantenibles. Al adoptar este enfoque arquitectónico y complementarlo con prácticas de desarrollo sólidas, los equipos de desarrollo pueden crear aplicaciones web de alta calidad que satisfagan las necesidades cambiantes de los usuarios y las empresas en el entorno digital actual.



Referencias.
Rick-Anderson. (2023, 13 julio). ASP.NET introducción MVC. Microsoft Learn. https://learn.microsoft.com/es-es/aspnet/mvc/overview/getting-started/

Diagramas de procesos en Visio - Soporte técnico de Microsoft. (s. f.). https://support.microsoft.com/es-es/topic/diagramas-de-procesos-en-visio-f064cd25-d7d5-47b8-87e1-ecb3c39cc165#:~:text=Los%20diagramas%20de%20proceso%20son,que%20indican%20el%20paso%20siguiente.
¿Qué es una aplicación web? - Explicación de las aplicaciones web - AWS. (s. f.). Amazon Web Services, Inc. https://aws.amazon.com/es/what-is/web-application/#:~:text=Una%20aplicaci%C3%B3n%20web%20es%20un,y%20de%20una%20forma%20segura.


