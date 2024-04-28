TECNOLÓGICO NACIONAL DE MÉXICO
INSTITUTO TECNOLÓGICO DE TLÁHUAC 
“LA ESENCIA DE LA GRANDEZA RADICA EN LAS RAICES”
INGENIERIA EN SISTEMA COMPUTACIONALES


El Modelo-Vista-Controlador (MVC)

DOCENTE: 
Cordeo Ocampo Martin Ramon
ESTUDIANTE: 
Ortiz Molina Ameyalli 
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
![Diagrama entidad relacion ER]()
