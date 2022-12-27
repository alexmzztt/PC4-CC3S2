# PC4-CC3S2

PREGUNTA 1

• ¿Se necesita la infraestructura SOA para integrar los dos nuevos servicios?

Sí, ya que al crearse los servicios para creación y ejecución de campañas y el segundo para 
evaluación de resultados de campañas, estos deben integrarse al 
sistema para que puedan ser usados correctamente por CMR y Integration & Orchestation, para 
esto sirve SOA, ya que permite que integren con mayor falicidad y seguridad, lo que es muy importante
al hablar de un sistema de correo electronico en este caso particular.

● El servicio de evaluación de campañas necesita manejar una gran cantidad de datos.
Sí, ya que este servicio se basa en medir que tanto se llegó al público con la campaña, por ejemplo 
dependiendo de que tipo de evaluacion se quiere hacer, si nuestro propósito es saber que tanto impacto 
se tuvo con el público, o que tanto recuerda el público nuestro producto, entre otros más factores son datos
estadisticos y contables, entonces la parte de evaluación necesita manipular una gran cantidad de datos para poder llegar a este resultado,
necesita evaluar para uno de los puntos por cliente al que se le envió el correo y luego trabajarlos
para llegar a un resultado general, claro que también hay plataformas que ya in cluyen esto como la publicidad
en marketplace que te da un resultado final de impacto de la campaña.

● ¿Sería mejor utilizar la replicación de datos, la integración a nivel de interfaz de usuario o las
llamadas de servicio para acceder a grandes cantidades de datos?

Si hablamos de una gran cantidad de datos entonces seria mejor utilizar las llamadas a servicio, ya que de esta forma
cada uno mantiene sus propios datos y se llaman solo a los necesarios, así evitamos
llamar datos no deseados,lo cual también lo hace escalable, a diferencia por ejemplo con la recopilación de datos, en la cual tendríamos muchos
datos innecesarios para cada tarea que querramos realizar, sin embargo debemos tener en cuenta que al final
cada uno tiene beneficios y desventajas y se decidirá según lo que requiera el sistema, por ejemplo escalabilidad, eficacia, rendimiento, etc.

● ¿Cuál de estas opciones de integración suele ofrecer SOA?

SOA ofrece los tres tipos de integración, sin embargo al hablar de SOA sabemos que tiene como objetivo la autonomia, reutilizacion, bajo acoplamiento,
comunmente orientada a servicios web pero no exclusiva para ello, entonces podemos decir que según esto 
las llamadas a servicios es lo que SOA suele ofrecer ya que cuenta con las carácteristicas escensiales de SOA.

● ¿Debe el servicio integrarse al portal existente o tener su propia interfaz de usuario?

Depende de lo que se necesite o se quiera lograr con el sistema, en este caso para la evaluacion de campaña 
yo recomendaría una interfaz de usuario propia ya que podría ser más beneficioso, por ejemplo si hablamos de 
comodidad para el usuario esta se puede diseñar de forma más érsonalizada, así la experiencia del usuario será
más agradable y cómoda, de forma que es más probable que siga usando nuestro sistema, lo cual es importante
al hablar de que tan fácil es de usar nuestro sistema así como la recurrencia de nuestros usuarios.

● ¿Cuáles son los argumentos a favor de cada opción?



PREGUNTA 3

Primero instalamos maven y verificamos con el comando `maven -v` que se haya instalado correctamente.

![maven_instalado](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/maven_instalado_prueba.jpg)

También debemos instalar docker y usamos el comando `docker ps` para confirmar que funciona correctamente.

![docker_instalado](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/docker_instalado_prueba.jpg)

Luego clonamos el repositorio de microservicios.

![microservices](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/clonar_microservice_repo.jpg)

Clonamos el repositorio de user registrarion para obtener la configuración.

![user-registration](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/clonar_user-registration-V2_repo.jpg)

Ejecutamos el comando `mvn package` para construir el proyecto.

![mvn_package_1](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/mvn_package_1.jpg)

A continuación se muestra que se construyó el correctamente el proyecto.

![mvn_package_2](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/mvn_package_2.jpg)
