# Propuesta TP DSW

## Grupo

### Integrantes

- 52818 - Barroso Bollero, Agustín
- 52962 - Taborda, Ignacio
- 52961 - Figueroa, Francisco Alejandro
- 52847 - Taborda, Santiago

### Repositorios

- [frontend app](https://github.com/GupCus/Descalifica2-front)
- [backend app](https://github.com/GupCus/Descalifica2-back)

## Tema

### Descripción

Descalifica2 es un sitio web dedicado principalmente a la Fórmula 1, donde podrás consultar el calendario de carreras, acceder a información detallada sobre cada evento y mantenerte al día con las noticias sobre automovilismo. El objetivo del sitio es mantener informada a toda la comunidad amante del deporte automotor, brindando las fechas de cada Gran Premio, dónde verlo en vivo, y datos sobre las escuderías participantes junto a sus pilotos. Los usuarios pueden crear un perfil personalizado, indicando su nombre, escuderías, circuitos y pilotos favoritos para adaptar su experiencia en la plataforma. Además, podrán participar en un foro donde intercambiar opiniones, debatir y compartir su pasión con otros fanáticos de la Fórmula 1.

### Modelo

![Imagen del modelo](https://github.com/GupCus/tp/blob/main/DC%20Descalifica2.drawio.png?raw=true)

## Alcance Funcional

### Alcance Mínimo

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Usuario<br>2. CRUD Circuito<br>3. CRUD Escudería<br>4. CRUD Temporada<br>5. CRUD Categoría<br>6. CRUD Piloto|
|CRUD dependiente|1. CRUD Carrera {depende de} CRUD Circuito<br>2. |
|Listado<br>+<br>detalle| 1. Listado de pilotos, puede ser filtrado por escudería. Muestra nombre completo del piloto y su foto => detalle muestra todos los datos del circuito <br> 2. Listado de circuitos, puede ser filtrado por continente o por tipo de circuito. Muestra nombre del circuito y su trazado => detalle muestra todos los datos del circuito.|
|CUU/Epic|1. Reservar una habitación para la estadía<br>2. Realizar el check-in de una reserva (falta hacer)|

Adicionales para Aprobación (falta hacer o pasar los de arriba)
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Tipo Habitacion<br>2. CRUD Servicio<br>3. CRUD Localidad<br>4. CRUD Provincia<br>5. CRUD Habitación<br>6. CRUD Empleado<br>7. CRUD Cliente|
|CUU/Epic|1. Reservar una habitación para la estadía<br>2. Realizar el check-in de una reserva<br>3. Realizar el check-out y facturación de estadía y servicios|

### Alcance Adicional Voluntario

_Nota_: El Alcance Adicional Voluntario es opcional, pero ayuda a que la funcionalidad del sistema esté completa y será considerado en la nota en función de su complejidad y esfuerzo.

| Req      | Detalle                                                                                                                                                                                                             |
| :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Listados | 1. Estadía del día filtrado por fecha muestra, cliente, habitaciones y estado <br>2. Reservas filtradas por cliente muestra datos del cliente y de cada reserve fechas, estado cantidad de habitaciones y huespedes |
| CUU/Epic | 1. Consumir servicios<br>2. Cancelación de reserva                                                                                                                                                                  |
| Otros    | 1. Envío de recordatorio de reserva por email                                                                                                                                                                       |
