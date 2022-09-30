### Ejercicio práctico - NetCore/Node/Python - 2022-Q3

## Objetivo
Crear una API Rest para administrar la reserva y compra de un ticket aereo.

## Modelo
![](./modelo.jpg "Repositories model")

## Base de datos en memoria
Al cargar la aplicación, se inicializará los datos de la base inicial, la cual servirá como insumo para desarrollar el ejercicio.

---

## Indicaciones Generales

- Crear una rama con el nombre del participante: Ejemplo: Q32022-apellido1-appelido2-nombre1-nombre2.
- Subir cambios a sus ramas una vez terminado el tiempo establecido.
    - Al finalizar el tiempo el repositorio no permitirá nuevos cambios.
- El proyecto debe ser implementando con la metodologia TDD
- Elaborar Pruebas unitarias.
- Implementar buenas prácticas de programación.
- Implementar patrones de diseño.


---

## Ejercicio 1: Administración de Tickets 

<p><strong>Con el objetivo</strong> de poder administrar la compra de Tickets de una Aerolinea<br>
<strong>Como</strong> administrador de la plataforma<br>
<strong>Quiero</strong> tener una API que me permita reservar,editar la reserva y comprar</p>

#### Criterios de aceptación

- Crear Reserva:
<p><strong>Dado</strong> que envío los datos de una reserva<br>
<strong>Cuando</strong> consumo el servicio de creación de reserva<br>
<strong>Entonces</strong> se debe crear la reserva en la areolinea</p>

- Editar Reserva
<p><strong>Dado</strong> que modifico los datos una reserva<br>
<strong>Cuando</strong> consumo el servicio de actualización<br>
<strong>Entonces</strong> se debe actualizar la reserva en las fechas indicadas</p>


- Comprar Ticket Aereo
<p><strong>Dado</strong> que quiero comprar el ticket de la reserva realizada<br>
<strong>Cuando</strong> consumo servicio para crear ticket<br>
<strong>Entonces</strong> se debe generar el comprobante de compra y la reserva actualizar a confirmada</p>


#### Tareas

- Crear un endpoint para crear una reserva.
- Crear un endpoint para actualizar una reserva.
- Crear un endpoint para obtener una reserva por ID.
- Crear un endpoint para crear un ticket.

#### Expectativas técnicas del ejercicio

- Diseñar una API Rest con las operaciones básicas (CRUD).
- Arquitectura del proyecto.
- Buenas prácticas.
- Mapeado de entidad a un DTO (Data Transfer Object).
- Micro commits. 

---

### Ejercicio 2: Servicio para obtener las reservas confirmadas y sus ticket comprado.

<p><strong>Con</strong> el objetivo de obtener las reservas y su ticket comprado<br>
<strong>Como</strong> administrador de la plataforma<br>
<strong>Quiero</strong> tener servicio que me permita obtener las reservas y su ticket comprado</p>

#### Criterios de aceptación

- Criterio 1: Obtener las reservas y su ticket:

<p><strong>Dado</strong> que envío el rango de fecha inicial y fecha final<br>
<strong>Cuando</strong> consumo el servicio para obtener las reservas<br>
<strong>Entonces</strong> me retornará el detalle de las reservas creadas en ese periodo <br>
Y que se encuentren habilitados (state: Pendiente y Confirmada) <br>



#### Estructura de respuesta

```
{
	"reservas": [
		{
			"res_id": "1",
			"res_codigo": "RES-001",
			"cli_nombres": "Usuario1",			
			"res_estado": "Confirmada",
			"tic_codigo" : "TIC-001",
			"tic_total" : "1500"

		},
		{
			"res_id": "2",
			"res_codigo": "RES-002",
			"cli_nombres": "Usuario2",			
			"res_estado": "Confirmada",
			"tic_codigo" : "TIC-002",
			"tic_total" : "1500"
		}
	]
}
````

---


