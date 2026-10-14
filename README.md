# GESTIÓN HOTELERA

## Miembros del grupo L3-ABS-4

1. Romero Moreno, Iván
1. Arjona Montaño, Antonio Javier
1. García Galán, Jairo
1. Moreno Ureba, Ernesto

## 1. Introducción al problema
El cliente pide una aplicación donde se pueda manejar la gestión de un hotel, esto incluye: gestionar habitaciones libres, reservas, incidencias de esta, empleados y clientes.



Los usuarios de este proyecto será la dirección del hotel, empleados y clientes que hacen la reserva.

Los clientes serán las personas que hacen la reserva y que, además, podrán dejar una valoración sobre su estancia en el hotel, que la gestión podra ver.

Debido al reciente exito del hotel, la dirección ha decidido digitalizar el proceso de reserva y gestión de habitaciones, junto a la gestión de empleados.

Nuestras expectativas de cara al fin del proyecto es haber logrado la creación de una aplicación que sea efectiva a la hora de administrar el hotel.

## 2. Glosario de términos

### Cliente
Persona que puede realizar reservas de habitaciones, contratar servicios adicionales y realizar valoraciones sobre su estancia. Un cliente puede ser también empleado del hotel.

### Empleado
Persona que trabaja en el hotel y utiliza el sistema para realizar tareas relacionadas con la gestión de reservas, habitaciones, servicios o incidencias. Dependiendo de su puesto, puede desempeñar funciones de limpieza, recepción, mantenimiento, cocina, botones, aparcacoches o gerencia. Un empleado puede ser también cliente.

### Estado de la habitación
Situación en la que se encuentra una habitación en un momento determinado. Por ejemplo, puede estar disponible, ocupada o en mantenimiento.

### Estado de la incidencia
Situación en la que se encuentra una incidencia registrada en una habitación. Puede encontrarse pendiente, en curso o resuelta.

### Tipo de incidencia
El por qué de la incidencia. Hemos dividido las incidencias en necesita limpieza, plaga, daño mobiliario, desperfecto electricidad, desperfecto inmueble, problema de fontanería, desaparición de material y otras incidencias.

### Estado de la reserva
Situación en la que se encuentra una reserva. Entre los posibles estados se encuentran pendiente, confirmada, cancelada o finalizada.

### Habitación
Unidad de alojamiento del hotel que puede ser reservada por un cliente. Cada habitación dispone de un número, una planta, un tipo, una capacidad y un precio, además de un estado que indica su situación actual.

### Tipo de habitación
Las diferentes habitaciones disponibles para reservar en el hotel:
- Individual: Habitación que dispone de una cama individual, y un baño.
- Doble: Habitación que dispone con una cama de matrimonio y un baño.
- Doble con camas separadas: Habitación que dispone de dos camas individuales y un baño.
- Triple: Habitación con una cama de matrimonio, una cama individual y un baño.
- Cuádruple: Habitación con dos literas, dos camas en cada una y un baño.
- Premium: Habitación con dos camas de matrimonio separadas por una pared, con un baño para cada una. También cuenta con minibar y con acceso prioritario a los servicios del hotel.
  
### Incidencia
Problema, avería o situación anómala detectada en una habitación que requiere algún tipo de actuación por parte del personal del hotel. Las incidencias pueden tener diferentes niveles de prioridad (baja, media y alta)  y estados de resolución.

### Nacionalidad
Nacionalidad de un cliente.

### Número de huéspedes
Cantidad de personas que se alojarán en una reserva determinada. Este valor debe ser compatible con la capacidad de la habitación asignada.

### Puesto
Cargo que desempeña un empleado dentro del hotel. En el sistema se contemplan los puestos de limpiador, recepcionista, mantenimiento, cocinero, botones, aparcador de coches y gerente.

### Reserva
Registro mediante el cual un cliente solicita y obtiene la asignación de una habitación durante un periodo determinado. Una reserva incluye las fechas de entrada y salida, el número de huéspedes, su estado y el precio total.

### Servicio
Prestación adicional ofrecida por el hotel que puede ser contratada por los clientes durante una reserva. Cada servicio tiene un nombre, una descripción y un precio. Algunos ejemplos pueden ser el desayuno, el servicio de habitaciones o el aparcamiento.

### Valoración
Opinión que un cliente realiza sobre su experiencia asociada a una reserva. Incluye una puntuación de 1 a 5, un comentario y la fecha en la que se realiza.

### Usuario
Persona que dispone de una cuenta en el sistema del hotel. Un usuario puede tener el papel de cliente, de empleado o desempeñar ambos roles simultáneamente. También existe el rol del administrador, el cual tendrá acceso total a cualquier dato.


## 3. Visión general del sistema

### 3.1. Requisitos generales
RG1:El cliente debe poder revisar sus reservas, consultar la fecha, hora de entrada, hora de salida, tipo de habitación,servicios incluidos y coste total.

RG2: La dirección del hotel debe poder ver las habitaciones con incidencias y si se han resuelto o están en curso y las reservas asignadas a esa habitación.

RG3: Los clientes y administradores pueden ver las valoraciones de las habitaciones y servicios.

RG4: Los empleados del hotel deben poder consultar las incidencias, su orden de prioridad y el estado en el que se encuentran y añadir nuevas

RG5: Empleados y clientes pueden acceder a sus datos personales, la dirección a los de todos los usuarios del sistema

### 3.2. Usuarios del sistema

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Título requisito funcional

##R.F.01. Consulta de reservas de un cliente

Como cliente,

quiero consultar mis reservas para,

conocer las fechas, la habitación asignada, los servicios contratados y el precio total.

Prueba de aceptación

-Comprobar que se muestran las reservas asociadas al cliente que realiza la consulta.

-Comprobar que cada reserva muestra las fechas de entrada y salida, la habitacion asignada, los servicios contratados y el precio total.


##R.F.02. Listado de habitaciones

Como empleado,

quiero consultar el listado de habitaciones del hotel,

para conocer sus características y su estado actual.

Prueba de aceptación

-Comprobar que se muestran las habitaciones registradas en el sistema.

-Comprobar que cada habitación muestra su número, planta, tipo, capacidad, precio y estado.


##R.F.03. Consulta de habitaciones disponibles

Como recepcionista,

quiero consultar las habitaciones disponibles para un intervalo de fechas,

para informar a los clientes sobre las opciones de alojamiento.

Prueba de aceptación

-Comprobar que se muestran las habitaciones que no tienen reservas que se solapen con el intervalo consultado.

-Comprobar que no se muestran habitaciones en mantenimiento ni habitaciones afectadas por incidencias sin resolver que impidan su reserva.

-Se deben aplicar las reglas de negocio R.N.02, R.N.04 y R.N.10.


##R.F.04. Listado de incidencias

Como empleado,

quiero consultar las incidencias registradas en el hotel,

para conocer los problemas detectados en las habitaciones.

Prueba de aceptación

-Comprobar que se muestran las incidencias registradas en el sistema.

-Comprobar que cada incidencia muestra su fecha, descripción, estado, prioridad y habitación afectada.


##R.F.05. Consulta de incidencias pendientes

Como gerente,

quiero consultar las incidencias pendientes y en curso,

para supervisar los problemas que todavía no se han resuelto.

Prueba de aceptación

-Comprobar que se muestran las incidencias cuyo estado es pendiente o en curso.

-Comprobar que las incidencias resueltas no aparecen en los resultados.


##R.F.06. Consulta de reservas de una habitación

Como gerente,

quiero consultar las reservas asociadas a una habitación,

para conocer su historial de ocupación.

Prueba de aceptación

-Comprobar que se muestran las reservas asociadas a la habitación seleccionada.

-Comprobar que cada reserva muestra las fechas de entrada y salida, el número de huéspedes y el estado de la reserva.


##R.F.07. Listado de servicios

Como cliente,

quiero consultar los servicios ofrecidos por el hotel,

para conocer sus características y precios antes de contratarlos.

Prueba de aceptación

-Comprobar que se muestran los servicios incluidos en el catálogo del hotel.

-Comprobar que cada servicio muestra su nombre, descripción y precio.


##R.F.08. Consulta de empleados

Como gerente,

quiero consultar el listado de empleados del hotel,

para conocer su información laboral y el puesto que desempeñan.

Prueba de aceptación

-Comprobar que se muestran los empleados registrados en el sistema.

-Comprobar que se visualizan el NSS, el puesto y el salario de cada empleado.

-Comprobar que solo los usuarios autorizados pueden consultar la información laboral restringida.


##R.F.09. Consulta de valoraciones

Como gerente,

quiero consultar las valoraciones realizadas por los clientes,

para conocer su grado de satisfacción con las estancias en el hotel.

Prueba de aceptación

-Comprobar que se muestran las valoraciones registradas, incluyendo puntuación, comentario y fecha.

-Comprobar que cada valoración se puede relacionar con la reserva a la que pertenece.

-Se deben aplicar las reglas de negocio R.N.05, R.N.06 y R.N.07.


##R.F.10. Consulta de reservas por fechas

Como recepcionista,

quiero consultar las reservas correspondientes a un intervalo de fechas,

para conocer la actividad prevista del hotel durante ese periodo.

Prueba de aceptación

-Comprobar que se muestran las reservas que coinciden con el intervalo temporal consultado.

-Comprobar que cada resultado muestra las fechas de entrada y salida, el estado de la reserva y la habitación asignada.

-Se debe aplicar la regla de negocio R.N.02.

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

##### R.N.01. Fechas de una reserva
La fecha de salida de una reserva deberá ser posterior a la fecha de entrada.

##### R.N.02. Solapamiento de reservas
Una misma habitación no podrá estar asignada a dos reservas cuyos periodos de estancia se solapen.

##### R.N.03. Capacidad de la habitación
El número de huéspedes de una reserva no podrá superar la capacidad máxima de la habitación.

##### R.N.04. Estado de la habitación
Una habitación que se encuentre en mantenimiento no podrá ser asignada a una nueva reserva.

##### R.N.05. Valoración de una reserva
Una reserva podrá tener como máximo una valoración por cliente.

##### R.N.06. Puntuación de una valoración
La puntuación de una valoración deberá estar comprendida entre 1 y 5.

##### R.N.07. Valoración de una estancia
Una valoración solo podrá realizarse cuando la estancia correspondiente haya finalizado.

##### R.N.08. Gestión de incidencias
Una incidencia solo podrá ser gestionada por un empleado del hotel. Una incidencia podrá permanecer sin empleado asignado mientras esté pendiente.

##### R.N.09. Asignación de incidencias
Una incidencia que esté en estado resuelta no podrá ser asignada posteriormente a un empleado para su gestión.

##### R.N.10. Incidencias de una habitación en mantenimiento:
Una habitación que tenga una incidencia no resuelta no podrá estar disponible para nuevas reservas hasta que haya sido resuelta.


### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

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


