1.	INTRODUCCIÓN

ESTE ES UN PROYECTO FICTICIO USADO COMO PORTAFOLIO

En un mercado cada vez más competitivo y en constante evolución, la eficiencia operativa es fundamental para cualquier empresa.
Esta solución de software aborda el problema que cualquier empresa dedicada a la entrega de paquetes puede enfrentar, desde problemas con la optimización de sus procesos logísticos
que le impiden cumplir con las expectativas de los clientes y mantener su posición en el mercado, hasta la reducción de pérdidas económicas, mejorar la eficiencia 
y la calidad de los servicios de entrega de la empresa. Este software brinda a la empresa una herramienta integral para optimizar todas las etapas del proceso de entrega de paquetes, 
desde la recepción del pedido hasta la entrega final al cliente. 
Este informe proporciona una visión general del proceso de desarrollo de software, sus características clave y beneficios esperados para la empresa. 

2 DESCRIPCIÓN DEL NEGOCIO Y REQUERIMIENTOS

Se ideó una solución para una empresa que cumple con esta estructura: distribuye 3 tipos de paquete (frágil, común y bulto) en todos los departamentos de Uruguay utilizando como medio de transporte: auto, moto o camión.

Los usuarios del sistema son: Empleado (Chofer, Administrativo) y Clientes. Para autenticarse requieren nombre de usuario y clave de acceso. Luego de logueado cada usuario, accederá a la base de datos con el usuario SQL asociado a ese mismo usuario logueado.


ROL DE CADA USUARIO EN EL SISTEMA:

2.1. Actores primarios
A continuación se detallan los actores y las tareas que va a ejecutar cada uno en el Sistema.

Chofer:
●	Cambio de Estado de Paquetes
●	Logueo


Administrativo:

●	CRUD de Administrativos

●	CRUD Choferes

●	CRUD Empresas

●	CRUD de Paquetes

●	CRUD de Vehículos

●	CRUD de Solicitudes

●	Sanciones y suspensiones a Chofer

●   Multas (asociadas a Vehículo y Chofer)


3.	TECNOLOGÍAS 


3.1. BACK END Y SERVICIO 

3.1.1 SQL Server 2014

Pros de utilizar esta tecnología:
1 – Escalabilidad: SQL Server es conocido por ser capaz de manejar grandes cantidades de datos y escalabilidad vertical y horizontal. Puede crecer según las necesidades de la aplicación.

2 - Seguridad: Proporciona cifrado de datos, autenticación integrada y control de acceso. Es fundamental para proteger la confidencialidad de los datos sensibles.

3 – Integración con otras herramientas de Microsoft: SQL Server se integra bien con otras herramientas y tecnologías de Microsoft, como .NET Framework, Visual Studio y Azure.
Esto permite desarrollar e implementar soluciones completas.

4 – Administración de datos: ofrece una amplia gama de herramientas de administración para respaldar tareas como copias de seguridad, recuperación ante desastres, mantenimiento de bases de datos y optimización de consultas.												
Contras de utilizar esta tecnología:
1 - 	Costo: puede ser costoso, especialmente para empresas pequeñas o startups.  	    
Además puede requerir hardware potente.

2 – Plataforma específica: se puede ejecutar en Windows y Linux, pero es específica de Windows. Esto puede limitar la flexibilidad.

3 – Curva de aprendizaje: para los nuevos usuarios, la curva de aprendizaje puede ser pronunciada.

4 – Requisitos de recursos: puede requerir una cantidad significativa de recursos de hardware y software, significando un desafío para pequeñas empresas. 			



Porqué SQL SERVER?

   Esta tecnología resultó ser muy efectiva al momento de desarrollar y poner en funcionamiento la base de datos. 
   Es segura y es capaz de administrar datos eficazmente. 
   La curva de aprendizaje fue casi nula gracias a la experiencia previa y contrariamente a lo expresado en la literatura general, 
   no se necesitó un hardware potente para ejecutarla. Esta tecnología aportó un gran valor al proyecto.


3.1.2 SERVIDOR IIS ALOJADO LOCALMENTE
1 – Se integra muy bien con Windows y es la opción por defecto para el alojamiento de aplicaciones web en el entorno de Windows Server.		

2 – Rendimiento: tiene un rendimiento sólido y es capaz de manejar cargas pesadas de trabajo. Esta optimizado para trabajar con tecnologías Microsoft. 

3 – Seguridad: ofrece muchas opciones de seguridad, como autenticación integrada, autenticación basada en roles, cifrado SSL/TLS, protección contra ataques.

4	– Herramientas de administración: brinda herramientas de administración robustas, como el administrador de IIS.

	

1 – Curva de aprendizaje: como ya se posee experiencia previa, el aprendizaje para este proyecto no fue necesario.

Se eligió esta tecnología porque se esta trabajando con aplicaciones nativas Microsoft, y éste servidor es ideal para ejecutarlas todas.	

La url del servidor es:   http://ansuz.ddns.net


3.3 FRONT END
3.3.1 Xamarin  

1 - Desarrollo multiplataforma: Xamarin permite el desarrollo de aplicaciones móviles para iOS, Android y Windows usando un único código base en C#, 
aprovechando asi el backgroud de conocimientos adquiridos en C# a lo largo de la carrera.

2 – Acceso completo a APIs nativas de cada plataforma (iOS, Windows y Android) usando los SDK nativos.

3 – Reutilización de código: Xamarin usa un solo lenguaje de programación (C#) y un solo código base, se puede reutilizar gran parte del código entre plataformas (Windows, iOS y Android), 
acelerando mucho el proceso de desarrollo y reduciendo costos.

4 – Integración con Visual Studio: Xamarin se integra perfectamente con Visual Studio permitiendo el acceso a todas las características y herramientas de desarrollo.



1 – Curva de aprendizaje 
Para este proyecto al inicio la curva de aprendizaje fue muy grande, debido al desconocimiento de desarrollo de APIs (solo WCF a lo largo de la carrera), 
se debió aprender a programar de forma sincrónica y asincrónica y a desarrollar y conectar con la API.

2 – Compatibilidades y actualizaciones
Problemas de compatibilidad porque depende de los cambios y actualizaciones de las plataformas nativas iOS y Android. Pueden haber demoras en la disponibilidad de las compatibilidades con esas aplicaciones. 																				
Porque se eligió?
-	Porque ya se conocía de antemano el lenguaje C#.
-	Es multiplataforma y se puede tener acceso a las API nativas de iOS y Android.
-	Una vez dominados los fundamentos de Xamarin, es un lenguaje con mucho potencial										


3.3.2 Sitio WEB

Se decidió por la tecnología ASP.NET MVC como tecnología de front end por sus numerosos beneficios y capacidades.
Ofrece un enfoque estructurado y flexible para el desarrollo web con el patrón Modelo – Vista – Controlador. Permite separa claramente las responsabilidades facilitando el manejo del código y la colaboración en equipos de desarrollo. 

¿Porqué ASP.NET ?
Además permite controlar la creación de código HTML, CSS y JavaScript para personalizar la interfaz de usuario. Haciendo uso de esta habilidad para integrar bibliotecas y frameworks frontend, fue como se fusionó el código Razor con JavaScript para mostrar el mapa al ingresar un nuevo Paquete al Sistema.  


3.4 TECNOLOGÍAS DE SOPORTE

3.4.1 SOFTWARE

3.4.1.1 IDE

3.4.1.2 Visual Studio 2022


1 - Visual ofrece un entorno completo integrado completo para el desarrollo de software, que incluye herramientas de edición de código, depuración, compilación y gestión de proyectos.
2 – soporte multiplataforma: Visual es compatible con una amplia gama de tecnologías, como ser: C#, .NET, C++, JavaScript, Python, y muchas mas. Permite desarrollar aplicaciones para diferentes plataformas: Windows, web, mobiles y cloud.

3 – amplia comunidad y soporte.
Cuenta con una gran comunidad de desarrolladores y una amplia gama de recursos de aprendizaje, documentación  y soporte en línea.

1 – consumo de recursos: puede ser exigente en proyectos grandes, afectando el rendimiento. En este proyecto, el emulador de android tardaba entre 30 y 40 minutos en iniciarse, corriendo en un equipo Core I3 de 12 Gb de Ram,

2 – la curva de aprendizaje puede ser muy importante para nuevos desarrolladores de nuevas tecnologías y/o lenguajes.

Porque se eligió?

Se eligió Xamarin porque ya se tenía conocimiento de C# y programar en Android fue mucho más amigable.
				
	
3.4.1.2.2. Virtualización de Windows

3.4.1.2.2.1 VMWare 

1 -  Virtualización es muy eficiente, emulando perfectamente el sistema operativo Windows que fue el utilizado en este proyecto

2 – Amplia compatibilidad: es compatible con muchos sistemas operativos

3 – Funciones avanzadas: ofrece características como migración en caliente (trasladar la máquina virtual a un nuevo host sin apagarla), alta disponibilidad, recuperación ante desastres, 

4 – En la virtualización se ejecutan efectivamente:
-	Servidor IIS
-	BD de SQL Server Consumida por el sItio web y la Api
-	Sitio Web que consume la BD
-	La API consumida por la App móvil 	
		


Contras:

1 – Para usuarios novatos puede ser compleja la configuración y la implementación, en el caso de este proyecto ya se contaba con experiencia previa virtualizando sistemas Windows.

2 – Requisitos de hardware: puede requerir hardware específico y potente aumentando los costos y limitando la escalabilidad a pequeñas organizaciones.

 A pesar de las contras, se utilizó este virtualizador porque se tiene experiencia en anteriores implementaciones con muy buen funcionamiento y disponibilidad de todos los servicios.
	

 3.4.1.3. NO IP
 
Se utilizó este software para transformar la IP dinámica que da internet en una IP estática que es necesaria para poder acceder desde internet al Servidor IIS y sus aplicaciones.	               
			
1 – Fácil configuración	

1 – Posibles problemas de fiabilidad: al depender de un servicio de terceros para asignar un nombre de dominio a una dirección IP dinámica, existe el riesgo de posibles interrupciones del servicio.

2 – Seguridad: al utilizar un servicio de DNS dinámico es necesario garantizar la seguridad de los dispositivos y servicio conectados, especialmente si se accede a ellos desde internet.

Se utilizó porque es la opción ideal para obtener una IP fija.


3.4.1.4. API de Google Maps
Se eligió la integración al proyecto de la API de Google Maps por ser una opción poderosa y versátil para aprovechar los servicios de mapeo y geolocalización. 
Ofrece una amplia gama de funcionalidades desde visualización de mapas interactivos hasta geolocalización y rutas. Esto facilita mucho la tarea de los Choferes al momento de gestionar el pickup y entrega de paquetes. Está respaldada por el servicio y la infraestructura de Google lo que garantiza que siempre esté disponible y su rendimiento sea óptimo. Es la opción ideal para este proyecto.


3.4.1.5 JMETER
Las pruebas de carga y estrés son técnicas fundamentales en el desarrollo de software para evaluar el rendimiento de una aplicación en condiciones de carga simulada. 
JMeter es una herramienta de código abierto desarrollada por Apache y es muy popular para realizar estas pruebas. 
 JMeter simula el comportamiento de usuarios reales interactuando con el Sistema de forma simultánea aumentando considerablemente la carga de trabajo en los sistemas. Las pruebas de estrés implican someter la aplicación a cargas extremas para evaluar el comportamiento en condiciones límite llegando a su capacidad máxima, o superarla para identificar cuellos de botella.
3.4.1.6 Blazemeter

Es un plug in de Google Chrome, su función es grabar todas las interacciones del usuario con el explorador. Esas interacciones grabadas se pueden exportar a un archivo  .Jmx para poder ser ejecutados con JMeter. Entre otras cosas, se pueden grabar inicios de sesión para poder hacer cargas de estrés más específicas.  



3.5	Distribución del software

3.5.1	Versión en español

3.5.1.1	Web

https://ansuz.ddns.net/es

3.5.1.2	App Android descargable (para testing)

https://play.google.com/apps/testing/com.ansuzes.codecraft


3.5.2	Versión en inglés

3.5.2.1	Web

https://ansuz.ddns.net/en


3.5.2.2	App Android descargable (para testing)

https://play.google.com/apps/testing/com.ansuzen.codecraft

4.	Mi rol en el Proyecto
Me encargué completamente de todos los ciclos de desarrollo:
- Análisis y relevamiento de requerimientos
- Diseño funcional y técnico
- Desarrollo de ambas aplicaciones (Web y App Mobile)
- Integración de la base de datos y Servicios
- Pruebas y corrección de errores
- Publicación y mantenimiento


5.	Lecciones aprendidas

Fue un proyecto desafiante y enriquecedor del cual se pueden enumerar una serie de lecciones aprendidas:

– La gestión del tiempo y la dedicación fueron fundamentales, siendo necesario el enfoque a largo plazo y la perseverancia en la consecución de los objetivos a pesar de los desafíos.

– Durante el desarrollo fue necesario enfrentar momentos de frustración y estrés siendo necesario para enfrentar un proyecto a largo plazo.

– Se asumieron riesgos calculados, al enfrentar decisiones difíciles y al momento de elegir las tecnologías. Estos riesgos permitieron seguir avanzando y alcanzar las soluciones adecuadas.

– Fue necesario ser flexible ante los cambios y los desafíos que surgieron a lo largo del proyecto.

– Asumir riesgos en cuestiones técnicas desconocidas significó muchos errores  cometidos que fueron una valiosa enseñanza a lo largo de todo el proyecto. 

– Fue fundamental desarrollar la capacidad de análisis profundo para detectar problemas y encontrar soluciones alternativas.



8.	Documentación técnica disponible
Este proyecto cuenta con documentación completa de Ingeniería de Software (requerimientos, casos de uso, diagramas, diseño técnico y plan de pruebas).
Por razones de extensión y privacidad, no se publica aquí, pero puede solicitarse.


/----------COMO USAR EL SISTEMA------------/

DATOS DE ACCESO AL SISTEMA WEB:

usuario: ansuz

pass: aEr34! 


DATOS ACCESO APP MOBILE (usuario Chofer):

usuario: CREAR USUARIO

pass: CREAR PASS


DATOS ACCCESO CLIENTE (TIENE QUE REGISTRARSE EN EL SISTEMA)



