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

# Cliente
Persona que puede realizar reservas de habitaciones, contratar servicios adicionales y realizar valoraciones sobre su estancia. Un cliente puede ser también empleado del hotel.

# Empleado
Persona que trabaja en el hotel y utiliza el sistema para realizar tareas relacionadas con la gestión de reservas, habitaciones, servicios o incidencias. Dependiendo de su puesto, puede desempeñar funciones de limpieza, recepción, mantenimiento, cocina, botones, aparcacoches o gerencia. Un empleado puede ser también cliente.

# Estado de la habitación
Situación en la que se encuentra una habitación en un momento determinado. Por ejemplo, puede estar disponible, ocupada o en mantenimiento.

# Estado de la incidencia
Situación en la que se encuentra una incidencia registrada en una habitación. Puede encontrarse pendiente, en curso o resuelta.

# Tipo de incidencia
El por qué de la incidencia. Hemos dividido las incidencias en necesita limpieza, plaga, daño mobiliario, desperfecto electricidad, desperfecto inmueble, problema de fontanería, desaparición de material y otras incidencias.

# Estado de la reserva
Situación en la que se encuentra una reserva. Entre los posibles estados se encuentran pendiente, confirmada, cancelada o finalizada.

# Habitación
Unidad de alojamiento del hotel que puede ser reservada por un cliente. Cada habitación dispone de un número, una planta, un tipo, una capacidad y un precio, además de un estado que indica su situación actual.

# Tipo de habitación
Las diferentes habitaciones disponibles para reservar en el hotel:
- Individual: Habitación que dispone de una cama individual, y un baño.
- Doble: Habitación que dispone con una cama de matrimonio y un baño.
- Doble con camas separadas: Habitación que dispone de dos camas individuales y un baño.
- Triple: Habitación con una cama de matrimonio, una cama individual y un baño.
- Cuádruple: Habitación con dos literas, dos camas en cada una y un baño.
- Premium: Habitación con dos camas de matrimonio separadas por una pared, con un baño para cada una. También cuenta con minibar y con acceso prioritario a los servicios del hotel.
  
# Incidencia
Problema, avería o situación anómala detectada en una habitación que requiere algún tipo de actuación por parte del personal del hotel. Las incidencias pueden tener diferentes niveles de prioridad (baja, media y alta)  y estados de resolución.

# Nacionalidad
Nacionalidad de un cliente.

# Número de huéspedes
Cantidad de personas que se alojarán en una reserva determinada. Este valor debe ser compatible con la capacidad de la habitación asignada.

# Puesto
Cargo que desempeña un empleado dentro del hotel. En el sistema se contemplan los puestos de limpiador, recepcionista, mantenimiento, cocinero, botones, aparcador de coches y gerente.

# Reserva
Registro mediante el cual un cliente solicita y obtiene la asignación de una habitación durante un periodo determinado. Una reserva incluye las fechas de entrada y salida, el número de huéspedes, su estado y el precio total.

# Servicio
Prestación adicional ofrecida por el hotel que puede ser contratada por los clientes durante una reserva. Cada servicio tiene un nombre, una descripción y un precio. Algunos ejemplos pueden ser el desayuno, el servicio de habitaciones o el aparcamiento.

# Valoración
Opinión que un cliente realiza sobre su experiencia asociada a una reserva. Incluye una puntuación de 1 a 5, un comentario y la fecha en la que se realiza.

# Usuario
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

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

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

##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

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


