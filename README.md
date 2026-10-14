# GESTIÓN HOTELERA

## Miembros del grupo L3-ABS-4

1. Romero Moreno, Iván
2. Arjona Montaño, Antonio Javier
3. García Galán, Jairo
4. Moreno Ureba, Ernesto

## 1. Introducción al problema
El cliente pide una aplicación donde se pueda manejar la gestión de un hotel, esto incluye: gestionar habitaciones libres, reservas, incidencias de esta, empleados y clientes.

Los usuarios de este proyecto será la dirección del hotel, empleados y clientes que hacen la reserva.

Los clientes serán las personas que hacen la reserva y que, además, podrán dejar una valoración sobre su estancia en el hotel, que la gestión podra ver.

Debido al reciente exito del hotel, la dirección ha decidido digitalizar el proceso de reserva y gestión de habitaciones, junto a la gestión de empleados.

Nuestras expectativas de cara al fin del proyecto es haber logrado la creación de una aplicación que sea efectiva a la hora de administrar el hotel.

## 2. Glosario de términos

### Administrador
Usuario con acceso total a los datos del sistema. Puede consultar y gestionar usuarios, clientes, empleados, habitaciones, reservas, servicios, incidencias y valoraciones.

### Cliente
Persona que puede realizar reservas de habitaciones, contratar servicios adicionales y realizar valoraciones sobre su estancia. Un cliente puede ser también empleado del hotel.

### Empleado
Persona que trabaja en el hotel y utiliza el sistema para realizar tareas relacionadas con la gestión de reservas, habitaciones, servicios o incidencias. Su puesto determina sus funciones y permisos. Un empleado puede ser también cliente.

### Estado de la habitación
Situación en la que se encuentra una habitación en un momento determinado: disponible, ocupada o en mantenimiento.

### Estado de la incidencia
Situación en la que se encuentra una incidencia registrada en una habitación: pendiente, en curso o resuelta.

### Estado de la reserva
Situación en la que se encuentra una reserva: pendiente, confirmada, cancelada o finalizada.

### Gerente
Empleado responsable de supervisar el funcionamiento del hotel. Puede consultar las incidencias pendientes y en curso, las reservas de cada habitación, las valoraciones y la información laboral de los empleados.

### Habitación
Unidad de alojamiento del hotel que puede ser reservada por un cliente. Cada habitación dispone de un número, una planta, un tipo, una capacidad y un precio, además de un estado que indica su situación actual.

### Incidencia
Problema, avería o situación anómala detectada en una habitación que requiere una actuación por parte del personal del hotel. Tiene un tipo, una prioridad y un estado.

### Mantenimiento
Estado de una habitación que no puede ser reservada porque se está reparando o revisando.

### Nacionalidad
País del que es ciudadano un cliente. Es un dato que el hotel registra de sus huéspedes.

### NSS
Número de la Seguridad Social de un empleado. Es un dato laboral de acceso restringido.

### Número de huéspedes
Cantidad total de personas que se alojarán en una reserva, incluido el titular. Debe ser compatible con la capacidad de la habitación asignada.

### Precio total
Importe final de una reserva, calculado a partir del precio de la habitación durante las noches de estancia más el precio de los servicios contratados.

### Prioridad
Nivel de urgencia de una incidencia: baja, media o alta.

### Puesto
Cargo que desempeña un empleado: limpiador, recepcionista, mantenimiento, cocinero, botones, aparcador de coches o gerente.

### Reserva
Registro mediante el cual un cliente, que pasa a ser su titular, solicita y obtiene la asignación de una habitación durante un periodo determinado. Incluye las fechas de entrada y salida, el número de huéspedes, su estado y el precio total. La entrada se realiza siempre a las 14:00 y la salida a las 12:00.

### Salario
Retribución de un empleado. Es un dato laboral de acceso restringido.

### Servicio
Prestación adicional ofrecida por el hotel que puede ser contratada durante una reserva. Tiene un nombre, una descripción y un precio. Por ejemplo: desayuno, servicio de habitaciones o aparcamiento.

### Titular
Cliente que realiza una reserva y es responsable de ella. Cada reserva tiene un único titular, que es la persona que puede consultarla y, una vez finalizada, valorarla. El titular se aloja en la habitación y cuenta como un huésped más en el número de huéspedes de la reserva.

### Tipo de habitación
Categorías de habitación disponibles:
- *Individual:* una cama individual y un baño.
- *Doble:* una cama de matrimonio y un baño.
- *Doble con camas separadas:* dos camas individuales y un baño.
- *Triple:* una cama de matrimonio, una cama individual y un baño.
- *Cuádruple:* dos literas (cuatro camas individuales en total) y un baño.
- *Premium:* dos camas de matrimonio separadas por una pared, con un baño para cada una, minibar y acceso prioritario a los servicios del hotel.


### Tipo de incidencia
Motivo de la incidencia: necesita limpieza, plaga, daño de mobiliario, desperfecto de electricidad, desperfecto de inmueble, problema de fontanería, desaparición de material u otras incidencias.

### Usuario
Persona con una cuenta en el sistema. Puede tener el papel de cliente, de empleado o de ambos a la vez, o ser administrador.

### Valoración
Opinión que el titular de una reserva realiza sobre su experiencia asociada a ella. Incluye una puntuación de 0 a 5 con un máximo de un decimal, un comentario y la fecha en la que se realiza.


## 3. Visión general del sistema

### 3.1. Requisitos generales
**RG1.** El cliente debe poder consultar sus reservas, incluyendo las fechas de entrada y salida (con la hora de entrada, 14:00, y la de salida, 12:00), la habitación asignada, el tipo de habitación, los servicios contratados y el precio total.

**RG2.** El gerente debe poder consultar las habitaciones con incidencias, indicando si están pendientes, en curso o resueltas, y las reservas asociadas a cada habitación.

**RG3.** Los clientes, los empleados autorizados y los administradores deben poder consultar las valoraciones de las estancias.

**RG4.** Los empleados del hotel deben poder consultar las incidencias, su prioridad y su estado.

**RG5.** Cada usuario debe poder consultar sus propios datos personales.

**RG6.** El administrador debe poder consultar los datos de todos los usuarios del sistema.

### 3.2. Usuarios del sistema

En el sistema de gestión hotelera se distinguen tres tipos principales de usuarios: clientes, empleados y administradores.

#### Cliente

Es la persona que utiliza la aplicación para consultar sus reservas, conocer los servicios del hotel y consultar las valoraciones. También podrá realizar valoraciones de sus estancias una vez hayan finalizado. Tendrá acceso a sus propios datos personales y a la información de sus reservas.

#### Empleado

Es la persona que trabaja en el hotel y utiliza la aplicación para realizar las tareas correspondientes a su puesto. Podrá consultar la información necesaria para desempeñar sus funciones, como las habitaciones, las reservas o las incidencias. Dependiendo de su puesto, tendrá permisos específicos dentro del sistema.

Dentro de esta categoría se encuentra el gerente, que es el empleado responsable de supervisar el funcionamiento del hotel. Podrá consultar las incidencias pendientes y en curso, las reservas asociadas a las habitaciones, las valoraciones de los clientes y la información laboral de los empleados.

Los puestos (limpiador, recepcionista, mantenimiento, cocinero, botones, aparcador de coches y gerente) son especializaciones de empleado. Cada requisito funcional indica el puesto que realiza la consulta. Las funcionalidades asociadas a un puesto concreto solo están disponibles para ese puesto y para el administrador.

#### Administrador

Es el usuario que dispone de acceso total a los datos del sistema. Podrá consultar y gestionar la información almacenada en la base de datos, incluyendo usuarios, clientes, empleados, habitaciones, reservas, servicios, incidencias y valoraciones.

##### Compatibilidad entre roles

Una misma persona podrá ser cliente y empleado simultáneamente, tal como se establece en el glosario del proyecto. En ese caso, podrá utilizar las funcionalidades correspondientes a ambos roles.

## 4. Catálogo de requisitos

#### R.F.01. Consulta de reservas de un cliente
*Origen: RG1*

Como cliente,
quiero consultar mis reservas,
para conocer las fechas, la habitación asignada, los servicios contratados y el precio total.

**Prueba de aceptación**
- Comprobar que solo se muestran las reservas de las que el cliente que realiza la consulta es titular.
- Comprobar que cada reserva muestra las fechas de entrada y salida (con la hora de entrada, 14:00, y la de salida, 12:00), la habitación asignada con su tipo, los servicios contratados y el precio total.
- Comprobar que un cliente sin reservas ve un listado vacío.

#### R.F.02. Listado de habitaciones
*Origen: RG2*

Como empleado con puesto de recepción, limpieza, mantenimiento o gerente,
quiero consultar el listado de habitaciones del hotel,
para conocer sus características y su estado actual.

**Prueba de aceptación**
- Comprobar que se muestran todas las habitaciones registradas en el sistema.
- Comprobar que cada habitación muestra su número, planta, tipo, capacidad, precio y estado.

#### R.F.03. Consulta de habitaciones disponibles
*Origen: RG2*

Como empleado con puesto de recepción,
quiero consultar las habitaciones disponibles para un intervalo de fechas,
para informar a los clientes sobre las opciones de alojamiento.

**Prueba de aceptación**
- Comprobar que se muestran las habitaciones que no tienen reservas no canceladas que se solapen con el intervalo consultado (R.N.02).
- Comprobar que no se muestran habitaciones en mantenimiento (R.N.04).
- Comprobar que no se muestran habitaciones con incidencias pendientes o en curso (R.N.10).
- Comprobar que una habitación cuya reserva termina el día en que empieza el intervalo consultado sí se muestra como disponible.

#### R.F.04. Listado de incidencias
*Origen: RG4*

Como empleado con puesto de recepción, limpieza, mantenimiento o gerente,
quiero consultar las incidencias registradas en el hotel ordenadas por prioridad,
para atender primero las más urgentes.

**Prueba de aceptación**
- Comprobar que se muestran todas las incidencias registradas en el sistema.
- Comprobar que cada incidencia muestra su fecha, descripción, tipo, prioridad, estado, habitación afectada y empleado asignado (si lo tiene).
- Comprobar que el listado está ordenado de prioridad alta a baja.

#### R.F.05. Consulta de incidencias pendientes y en curso
*Origen: RG2*

Como gerente,
quiero consultar las incidencias pendientes y en curso,
para supervisar los problemas que todavía no se han resuelto.

**Prueba de aceptación**
- Comprobar que se muestran las incidencias cuyo estado es pendiente o en curso, indicando la habitación afectada.
- Comprobar que las incidencias resueltas no aparecen en los resultados.

#### R.F.06. Consulta de reservas de una habitación
*Origen: RG2*

Como gerente,
quiero consultar las reservas asociadas a una habitación,
para conocer su historial de ocupación.

**Prueba de aceptación**
- Comprobar que se muestran todas las reservas asociadas a la habitación seleccionada.
- Comprobar que cada reserva muestra las fechas de entrada y salida, el número de huéspedes y el estado de la reserva.

#### R.F.07. Listado de servicios
*Origen: RG1*

Como cliente,
quiero consultar los servicios ofrecidos por el hotel,
para conocer sus características y precios antes de contratarlos.

**Prueba de aceptación**
- Comprobar que se muestran todos los servicios del catálogo del hotel.
- Comprobar que cada servicio muestra su nombre, descripción y precio.

#### R.F.08. Consulta de empleados
*Origen: RG6*

Como gerente,
quiero consultar el listado de empleados del hotel,
para conocer su información laboral y el puesto que desempeñan.

**Prueba de aceptación**
- Comprobar que se muestran todos los empleados registrados en el sistema.
- Comprobar que se visualizan el NSS, el puesto y el salario de cada empleado.
- Comprobar que un empleado que no tiene el puesto de gerente, ni es administrador, no puede consultar el NSS ni el salario de otros empleados (R.N.15).

#### R.F.09. Consulta de valoraciones
*Origen: RG3*

Como gerente,
quiero consultar las valoraciones realizadas por los clientes,
para conocer su grado de satisfacción con las estancias en el hotel.

**Prueba de aceptación**
- Comprobar que se muestran las valoraciones registradas, incluyendo puntuación, comentario y fecha.
- Comprobar que cada valoración se puede relacionar con la reserva a la que pertenece.
- Comprobar que solo aparecen valoraciones de reservas finalizadas (R.N.07).

#### R.F.10. Consulta de reservas por fechas
*Origen: RG1*

Como empleado con puesto de recepción,
quiero consultar las reservas correspondientes a un intervalo de fechas,
para conocer la actividad prevista del hotel durante ese periodo.

**Prueba de aceptación**
- Comprobar que se muestran las reservas cuya estancia coincide con el intervalo consultado.
- Comprobar que cada resultado muestra las fechas de entrada y salida, el estado de la reserva y la habitación asignada.
- Comprobar que las reservas canceladas se muestran identificadas con su estado y no cuentan como ocupación de la habitación (R.N.02).

#### R.F.11. Consulta de valoraciones por parte de los clientes
*Origen: RG3*

Como cliente,
quiero consultar las valoraciones de otras estancias,
para conocer la opinión de otros huéspedes antes de reservar.

**Prueba de aceptación**
- Comprobar que se muestran la puntuación, el comentario y la fecha de cada valoración.
- Comprobar que no se muestran los datos personales del titular que realizó la valoración.

#### R.F.12. Consulta de datos personales propios
*Origen: RG5*

Como usuario del sistema,
quiero consultar mis datos personales,
para comprobar que la información que el hotel tiene de mí es correcta.

**Prueba de aceptación**
- Comprobar que el usuario ve únicamente sus propios datos.
- Comprobar que un usuario que es cliente y empleado a la vez ve los datos de ambos roles.

#### R.F.13. Consulta de datos de todos los usuarios
*Origen: RG6*

Como administrador,
quiero consultar los datos de todos los usuarios del sistema,
para gestionar la información de clientes y empleados.

**Prueba de aceptación**
- Comprobar que se muestran todos los usuarios registrados, con su rol (cliente, empleado o ambos).
- Comprobar que un usuario sin rol de administrador, incluido el gerente, no puede acceder a este listado.

#### R.F.14. Consulta de incidencias de una habitación
*Origen: RG2*

Como gerente,
quiero consultar las incidencias de una habitación concreta, incluidas las resueltas,
para conocer su historial de problemas.

**Prueba de aceptación**
- Comprobar que se muestran todas las incidencias de la habitación seleccionada, con estado pendiente, en curso o resuelta.
- Comprobar que no se muestran incidencias de otras habitaciones.

#### 4.1.1. Requisitos de información

##### R.I.01. Título requisito de información

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

#### R.N.01. Fechas de una reserva
La fecha de salida de una reserva deberá ser posterior a la fecha de entrada. La hora de entrada es siempre las 14:00 y la hora de salida siempre las 12:00.

**Prueba de aceptación**
- Crear una reserva con entrada el 10/10 y salida el 12/10: se acepta, con entrada a las 14:00 del 10/10 y salida a las 12:00 del 12/10.
- Crear una reserva con entrada y salida el mismo día: se rechaza.
- Crear una reserva con salida anterior a la entrada: se rechaza.
- Comprobar que cualquier reserva creada tiene hora de entrada 14:00 y hora de salida 12:00.

#### R.N.02. Solapamiento de reservas
Una misma habitación no podrá estar asignada a dos reservas no canceladas cuyos periodos de estancia se solapen. Dos periodos se solapan cuando la fecha de entrada de cada uno es anterior a la fecha de salida del otro, de modo que una reserva puede empezar el mismo día en que otra termina (la salida es a las 12:00 y la entrada a las 14:00).

**Prueba de aceptación**
- Reservar la habitación 101 del 10/10 al 15/10 y después del 12/10 al 14/10: la segunda se rechaza.
- Reservar la habitación 101 del 10/10 al 15/10 y después del 15/10 al 18/10: se acepta.
- Reservar la habitación 101 del 10/10 al 15/10, cancelar esa reserva y reservar del 12/10 al 14/10: se acepta.


#### R.N.03. Capacidad de la habitación
El número de huéspedes de una reserva, incluido el titular, deberá ser al menos 1 y no podrá superar la capacidad máxima de la habitación asignada.

**Prueba de aceptación**
- Reservar una habitación de capacidad 2 para 2 huéspedes (titular incluido): se acepta.
- Reservar una habitación de capacidad 2 para 3 huéspedes (titular incluido): se rechaza.
- Reservar una habitación de capacidad 2 para el titular y 2 acompañantes (3 huéspedes en total): se rechaza.
- Reservar cualquier habitación para 0 huéspedes: se rechaza.

#### R.N.04. Estado de la habitación
Una habitación que se encuentre en mantenimiento no podrá ser asignada a una nueva reserva.

**Prueba de aceptación**
- Intentar reservar una habitación en estado "mantenimiento": se rechaza.
- Intentar reservar una habitación en estado "disponible" con fechas libres: se acepta.

#### R.N.05. Valoración de una reserva
Una reserva podrá tener como máximo una valoración, y solo podrá realizarla su titular.

**Prueba de aceptación**
- El titular de una reserva finalizada sin valoración registra una valoración: se acepta.
- El mismo titular intenta registrar una segunda valoración para la misma reserva: se rechaza.
- Un cliente que no es el titular de la reserva intenta valorarla: se rechaza.

#### R.N.06. Puntuación de una valoración
La puntuación de una valoración deberá ser un número comprendido entre 0 y 5, ambos incluidos, con un máximo de un decimal.

**Prueba de aceptación**
- Registrar valoraciones con puntuación 0, 3,5 y 5: se aceptan.
- Registrar una valoración con puntuación 4,25 (dos decimales): se rechaza.
- Registrar una valoración con puntuación -0,5: se rechaza.
- Registrar una valoración con puntuación 5,1: se rechaza.

#### R.N.07. Valoración de una estancia
Una valoración solo podrá realizarse cuando la reserva correspondiente esté en estado "finalizada".

**Prueba de aceptación**
- Valorar una reserva "finalizada": se acepta.
- Valorar una reserva "pendiente", "confirmada" o "cancelada": se rechaza.

#### R.N.08. Gestión de incidencias
Una incidencia solo podrá ser asignada a un empleado del hotel. Mientras esté pendiente, podrá permanecer sin empleado asignado.

**Prueba de aceptación**
- Registrar una incidencia pendiente sin empleado asignado: se acepta.
- Asignar una incidencia a un usuario que es empleado: se acepta.
- Asignar una incidencia a un usuario que solo es cliente: se rechaza.

#### R.N.09. Asignación de incidencias
Una incidencia en estado "resuelta" no podrá asignarse posteriormente a un empleado.

**Prueba de aceptación**
- Asignar un empleado a una incidencia "en curso": se acepta.
- Asignar un empleado a una incidencia "resuelta": se rechaza.

#### R.N.10. Disponibilidad con incidencias sin resolver
Una habitación con una incidencia no resuelta (pendiente o en curso) no podrá asignarse a nuevas reservas hasta que dicha incidencia pase a "resuelta".

**Prueba de aceptación**
- Intentar reservar una habitación con una incidencia "pendiente": se rechaza.
- Intentar reservar una habitación con una incidencia "en curso": se rechaza.
- Marcar la incidencia como "resuelta" e intentar reservar de nuevo: se acepta.

#### R.N.11. Prioridad de una incidencia
La prioridad de una incidencia solo podrá ser baja, media o alta.

**Prueba de aceptación**
- Registrar incidencias con prioridad baja, media y alta: se aceptan.
- Registrar una incidencia con prioridad "urgente": se rechaza.

#### R.N.12. Estados de una reserva
Una reserva nace en estado "pendiente" y puede pasar a "confirmada" y después a "finalizada". Una reserva "pendiente" o "confirmada" puede pasar a "cancelada". Una reserva "finalizada" o "cancelada" no puede cambiar de estado.

**Prueba de aceptación**
- Pasar una reserva de "pendiente" a "confirmada": se acepta.
- Pasar una reserva de "confirmada" a "cancelada": se acepta.
- Pasar una reserva "cancelada" a "confirmada": se rechaza.
- Pasar una reserva "pendiente" directamente a "finalizada": se rechaza.

#### R.N.13. Precio total de una reserva
El precio total de una reserva será el precio de la habitación multiplicado por el número de noches, más la suma de los precios de los servicios contratados. El número de noches es la diferencia en días entre la fecha de entrada y la fecha de salida.

**Prueba de aceptación**
- Reserva de 3 noches en una habitación de 80 € sin servicios: el precio total es 240 €.
- Reserva de 3 noches en una habitación de 80 € con un servicio de 15 €: el precio total es 255 €.

#### R.N.14. Unicidad del NSS
Dos empleados no podrán tener el mismo NSS.

**Prueba de aceptación**
- Registrar un empleado con un NSS nuevo: se acepta.
- Registrar un segundo empleado con un NSS ya existente: se rechaza.

#### R.N.15. Acceso a la información laboral
El NSS y el salario de un empleado solo podrán ser consultados por el gerente y por el administrador.

**Prueba de aceptación**
- El gerente consulta el NSS y el salario de un empleado: se muestran.
- Un empleado sin rol de gerente intenta consultar el salario de otro empleado: se deniega.
- Un cliente intenta consultar datos laborales: se deniega.

#### R.N.16. Número de habitación
Cada habitación tendrá un número que la identifique y que no podrá repetirse en el hotel.

**Prueba de aceptación**
- Registrar la habitación 101 por primera vez: se acepta.
- Registrar otra habitación con el número 101: se rechaza.


### 4.2. Mapa de historias de usuario
**R.G. 01. Consulta de reservas
Como usuario,
quiero poder consultar los datos de mi reserva
para poder organizar mis estancia mejor

**R.G. 02. Consulta de datos de habitaciones
Como administrador,
quiero poder consultar que habitaciones estan disponibles
para poder realizar una correcta organización del hotel

**R.G. 03. Consulta de valoraciones
Como usuario del sistema
quiero poder ver las valoraciones de las habitaciones
para saber que cuales habitaciones son las mejores

**R.G. 04. Consulta de incidencias
Como empleado
quiero poder consultar las habitaciones con incidencias y el estado de estas
para poder solucionarlas lo antes posible

**R.G. 05 Consulta de datos personales
Como usuario
quiero consultar mis propios datos personales
para cambiarlos si es necesario

**R.G. 06 Administración de datos
Como administrador
quiero poder consultar los datos de todos los usuarios
para gestionar reservas de clientes y el trabajo de los empleados

**R.F.01. Consulta de reservas de un cliente
Como cliente, 
quiero consultar mis reservas,
para conocer las fechas, la habitación asignada, los servicios contratados y el precio total

**R.F.02. Listado de habitaciones
Como empleado con puesto de recepción, limpieza, mantenimiento o gerente, 
quiero consultar el listado de habitaciones del hotel, 
para conocer sus características y su estado actual

**R.F.03. Consulta de habitaciones disponibles
Como empleado con puesto de recepción,
quiero consultar las habitaciones disponibles para un intervalo de fechas,
para informar a los clientes sobre las opciones de alojamiento

**R.F.04. Listado de incidencias
Como empleado con puesto de recepción, limpieza, mantenimiento o gerente, 
quiero consultar las incidencias registradas en el hotel ordenadas por prioridad,
para atender primero las más urgentes

**R.F.05. Consulta de incidencias pendientes y en curso
Como gerente, 
quiero consultar las incidencias pendientes y en curso, 
para supervisar los problemas que todavía no se han resuelto

**R.F.06. Consulta de reservas de una habitación
Como gerente, 
quiero consultar las reservas asociadas a una habitación, 
para conocer su historial de ocupación

**R.F.07. Listado de servicios
Como cliente, 
quiero consultar los servicios ofrecidos por el hotel, 
para conocer sus características y precios antes de contratarlos

**R.F.08. Consulta de empleados
Como gerente, 
quiero consultar el listado de empleados del hotel, 
para conocer su información laboral y el puesto que desempeñan

**R.F.09. Consulta de valoraciones
Como gerente,
quiero consultar las valoraciones realizadas por los clientes, 
para conocer su grado de satisfacción con las estancias en el hotel.

**R.F.10. Consulta de reservas por fechas
Como empleado con puesto de recepción,
quiero consultar las reservas correspondientes a un intervalo de fechas,
para conocer la actividad prevista del hotel durante ese periodo

**R.F.11. Consulta de valoraciones por parte de los clientes
Como cliente, 
quiero consultar las valoraciones de otras estancias, 
para conocer la opinión de otros huéspedes antes de reservar

**R.F.12. Consulta de datos personales propios
Como usuario del sistema, 
quiero consultar mis datos personales, 
para comprobar que la información que el hotel tiene de mí es correcta

**R.F.13. Consulta de datos de todos los usuarios
Como administrador, 
quiero consultar los datos de todos los usuarios del sistema, 
para gestionar la información de clientes y empleados

**R.F.14. Consulta de incidencias de una habitación
Como gerente,
quiero consultar las incidencias de una habitación concreta, 
incluidas las resueltas, para conocer su historial de problemas

**R.N.01. Fechas de una reserva
Como administrador del hotel,
quiero que la fecha de salida sea siempre posterior a la de entrada
para un correcto funcionamiento de reservas del hotel

**R.N.02. Solapamiento de reservas
Como administrador
quiero que 2 reservas no se solapen
para evitar que varios clientes ocupen la misma habitación a la vez

**R.N.03. Capacidad de la habitación
Como administrador
quiero que el número de personas por reserva sea mayor o igual que uno
para evitar reservas sin personas

**R.N.04. Estado de la habitación
Como administrador
quiero saber el estado de las habitaciones
para no asignar una que este en mantenimiento

**R.N.05. Valoración de una reserva
Como administrador
quiero que solo exista una reseña por reserva
para evitar reseñas falsas

**R.N.06. Puntuación de una valoración
Como administrador
quiero que la puntuacion de la reserva este comprendida entre 1 y 5 con hasta una cifra decimal
para facilitar la lectura de la puntuacion de la reserva

**R.N.07. Valoración de una estancia
Como administrador 
quiero que la valoracion solo este disponible tras la finalización de la reserva
para evitar que los clientes reserven, hagan una valoración falsa y cancelen la reserva

**R.N.08. Gestión de incidencias
Como administrador
quiero que a cada incidencia le corresponda un empleado (o ninguno dependiendo de su estado)
para agilizar su resolución

**R.N.09. Asignación de incidencias
Como administrador
quiero que las incidencias resueltas no se les pueda asignar un empleado
para evitar que se intente resolver una incidencia inexistente

**R.N.10. Disponibilidad con incidencias sin resolver
Como administrador
quiero que una habitación con una incidencia no pueda ser asignada
para evitar estancias en una habitación en mantenimiento

**R.N.11. Prioridad de una incidencia
Como administrador
quiero que solo pueda haber tres tipos de prioridades para las incidencias

**R.N.12. Estados de una reserva
Como administrador
quiero que las reservas pendientes pueden pasar a confirmadas y a completadas, de comfirmada a cancelada, de pendiente a cancelada y que de cancelada no pueda pasar a ningún otro estado

**R.N.13. Precio total de una reserva
Como administrador
quiero calcular el precio de una habitación dependiendo del número de días de la estancia y los servicios contratados

**R.N.14. Unicidad del NSS
Como administrador
quiero que dos empleados no puedan compartir NSS
para evitar empleados duplicados

**R.N.15. Acceso a la información laboral
Como administrador
quiero que los datos de salario y NSS de los empleados sean accesible solo para los administradores
para la protección de datos

**R.N.16. Número de habitación
Como administrador
quiero que el número de las habitaciones sean únicos
para evitar habitaciones repetidas
### 4.3. Requisitos no funcionales

**R.N.F. 01. Protección de datos personales**
Como usuario del sistema
quiero que mis datos personales solo puedan ser consultados por mí o por el administrador
para que mi información personal esté protegida

**R.N.F. 02. Confidencialidad de la información laboral**
Como empleado del hotel
quiero que mi NSS y mi salario solo puedan ser consultados por el gerente y el administrador
para que mi información laboral sea confidencial

**R.N.F. 03. Autenticación**
Como administrador
quiero que todo acceso al sistema requiera identificarse con usuario y contraseña
para que solo las personas autorizadas puedan utilizarlo

**R.N.F. 04. Control de acceso por rol y puesto**
Como administrador
quiero que cada usuario solo pueda utilizar las funcionalidades de su rol y, en el caso de los empleados, de su puesto
para evitar accesos a información que no le corresponde

**R.N.F. 05. Rendimiento**
Como empleado del hotel
quiero que las consultas y listados se muestren en menos de 3 segundos
para poder atender a los clientes sin esperas
//Se puede quitar si es muy ambiciosa para lo que haremos tecnicamente

**R.N.F. 06. Usabilidad**
Como empleado del hotel
quiero poder utilizar el sistema sin formación técnica previa
para realizar mis tareas desde el primer día

-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


