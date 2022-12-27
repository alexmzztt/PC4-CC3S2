# PC4-CC3S2

## PREGUNTA 1

### • ¿Se necesita la infraestructura SOA para integrar los dos nuevos servicios?

Sí, ya que al crearse los servicios para creación y ejecución de campañas y el segundo para 
evaluación de resultados de campañas, estos deben integrarse al 
sistema para que puedan ser usados correctamente por CMR y Integration & Orchestation, para 
esto sirve SOA, ya que permite que integren con mayor falicidad y seguridad, lo que es muy importante
al hablar de un sistema de correo electronico en este caso particular.

### ● El servicio de evaluación de campañas necesita manejar una gran cantidad de datos.
Sí, ya que este servicio se basa en medir que tanto se llegó al público con la campaña, por ejemplo 
dependiendo de que tipo de evaluacion se quiere hacer, si nuestro propósito es saber que tanto impacto 
se tuvo con el público, o que tanto recuerda el público nuestro producto, entre otros más factores son datos
estadisticos y contables, entonces la parte de evaluación necesita manipular una gran cantidad de datos para poder llegar a este resultado,
necesita evaluar para uno de los puntos por cliente al que se le envió el correo y luego trabajarlos
para llegar a un resultado general, claro que también hay plataformas que ya in cluyen esto como la publicidad
en marketplace que te da un resultado final de impacto de la campaña.

### ● ¿Sería mejor utilizar la replicación de datos, la integración a nivel de interfaz de usuario o las
llamadas de servicio para acceder a grandes cantidades de datos?

Si hablamos de una gran cantidad de datos entonces seria mejor utilizar las llamadas a servicio, ya que de esta forma
cada uno mantiene sus propios datos y se llaman solo a los necesarios, así evitamos
llamar datos no deseados,lo cual también lo hace escalable, a diferencia por ejemplo con la replicación de datos, en la cual tendríamos muchos
datos innecesarios para cada tarea que querramos realizar, sin embargo debemos tener en cuenta que al final
cada uno tiene beneficios y desventajas y se decidirá según lo que requiera el sistema, por ejemplo escalabilidad, eficacia, rendimiento, etc.

### ● ¿Cuál de estas opciones de integración suele ofrecer SOA?

SOA ofrece los tres tipos de integración, sin embargo al hablar de SOA sabemos que tiene como objetivo la autonomia, reutilizacion, bajo acoplamiento,
comunmente orientada a servicios web pero no exclusiva para ello, entonces podemos decir que según esto 
las llamadas a servicios es lo que SOA suele ofrecer ya que cuenta con las carácteristicas escensiales de SOA.

### ● ¿Debe el servicio integrarse al portal existente o tener su propia interfaz de usuario?

Depende de lo que se necesite o se quiera lograr con el sistema, en este caso para la evaluacion de campaña 
yo recomendaría una interfaz de usuario propia ya que podría ser más beneficioso, por ejemplo si hablamos de 
comodidad para el usuario esta se puede diseñar de forma más érsonalizada, así la experiencia del usuario será
más agradable y cómoda, de forma que es más probable que siga usando nuestro sistema, lo cual es importante
al hablar de que tan fácil es de usar nuestro sistema así como la recurrencia de nuestros usuarios.

### ● ¿Cuáles son los argumentos a favor de cada opción?

Integrarse al portal existente: tiene como beneficio el usar el diseño ya existente y que los usuarios no 
usen y tengan que adecuarse a otra interfaz, tambien facilita el trabajo, administración
 y mantenimiento del servicio. También es más barato para el cliente ya que no se creará una interfaz personalizada.

Interfaz ded usuario propia: es más cómoda, amigable y flexible para el usuario, la experiencia del usuario 
puede mejorar en gran medida ya que la interfaz de realizará a las necesidades que este tenga, también hace que 
el sistema sea más escalable y de esta forma será más fácil poder hacer cambios fututos.

### ● ¿Deberías implementar la nueva funcionalidad, el equipo de CRM?

Esto depende de si el equipo se encuentra capacitado para manejar dicha funcionalidad, en este caso el 
equipo de CMR considero que si cuenta con conocimientos y habilidades para manejarlo, sin embargo también 
recomendaría un par de especialistas en ello, así el equipo sería más variado y se tendrían diferentes perspectivas,
con esto el equipo original al haber sido parte de todo el proceso tiene conocimiento de fallos y aciertos en 
cuanto al desarrollo del sistema y el nuevo personal también sería valioso por la nueva vista que puede bridar al proyecto,
algo importante también es tomar en cuenta la integración de la nueva funcionalidad y que tan provechoso sea, 
los beneficios que esta nos va a aportar, si cumple con las necesidades del cliente y al final el costo también 
es un factor importante y decisivo, en este caso evaluando todo ello considero que si se deberia implementar la nueva funcionalidad
 ya que trae consigo muchos beneficios.

## PREGUNTA 2

En un sistema basado en microservicios puede haber diferentes tipos de comunicación; sin embargo,
debe haber un tipo de comunicación predominante.¿Cuál escogerías?¿Qué otros están permitidos
además?¿En qué situaciones?
¿Utilizarías la replicación de datos en un sistema basado en microservicios?¿En qué áreas?¿Cómo lo
implementarías?

### ¿Cuál escogerías?

Comunicación asíncrona, de esta forma se tiene autonomía y mientras menos comunicación se tenga entre
microservicios mejor, ya que el objetivo de los microservicios es ser autónomos y no depender de otros microservicios 
como lo sería con una comunicaión síncrona de solicitud y respuesta, si usamos comunicación síncrona esta crearía 
una cadena de solicitudes y respuestas lo cual termina generando demora y poca eficiencia comparado con la comunicación
asíncrona que brinda autonomía a los microservicios. Una de las principales opciones sería REST API.

### ¿Qué otros están permitidos además?¿En qué situaciones?

Comunicación síncrona: cuando se usa el mecanismo de solicitud y respuesta, se usa para consultar datos de una interfaz
 de usuario activa, o sea en tiempo real, desde aplicaciones cliente, esto mediante comunicacion solicitud-respuesta 
y REST.

RPC (Remote Procedure Call): nos va a permitir ejecutar un servicio en un servidor remoto, y la respuesta de la solicitud
se recibe en el mismo formato de la que se envía. Un ejemplo sería gRPC (Google Remote Procedure Call).

### ¿Utilizarías la replicación de datos en un sistema basado en microservicios?¿En qué áreas?¿Cómo lo
implementarías?

Sí, la replicacion de datos si bien duplica los daatos, en casos donde el acceso a estos sea necesario por ejemplo si se
ejecutan en diferentes dispositivos, esta duplicación en cada uno de los dispositivos va a permitir que cada maquina pueda 
tener acceso local a los datos, asi los datos están disponibles en cada maquina y no dependen de otra para conseguirlos, por 
ejemplo esto se podria implementar en los sistemas de bases de datos.

## PREGUNTA 3

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

## PREGUNTA 4

### ACTIVIDAD 21

Un hello world de varias estapas

![codigo_pipeline1](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/codigo_pipeline1.jpg)

![pipeline_stageview](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/pipeline_stageview.jpg)

![salida_de_consola_1](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/salida_de_consola_1.jpg)

Para el segundo pipeline

![codigo_pipeline2](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/codigo_pipeline2.jpg)

![pipeline2_stageview](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/pipeline2_stageview.jpg)

Calculator

![codigo_calculator](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/codigo_calculator.jpg)

![calculatorbuild](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/calculatorbuild.jpg)

Para compile

![startspringio](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/startspringio.jpg)

![archivoscalculatorclone](https://github.com/alexmzztt/PC4-CC3S2/blob/main/.assets/archivoscalculatorclone.jpg)






