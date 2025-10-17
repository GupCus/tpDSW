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

![Imagen del modelo](https://github.com/GupCus/tpDSW/blob/main/ModeloBDDescalifica2.jpg)
## Alcance Funcional

### Alcance Mínimo

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Circuito<br>2. CRUD Marca<br>3. CRUD Temporada<br>4. CRUD Categoría|
|CRUD dependiente|1. CRUD Carrera<br>2. CRUD Sesion <br>3. CRUD Piloto|
|Listado<br>+<br>detalle| 1. Listado de pilotos, puede ser filtrado por escudería. => Detalle muestra nombre completo del piloto y su foto <br> 2. Listado de circuitos, puede ser filtrado por país y muestra su trazado => Detalle muestra todos los datos del circuito.<br> 3. Listado de temporadas, muestra todas las carreras pasadas junto a sus sesiones ⇒ Detalle muestra todos los detalles de una carrera y posiciones en las sesiones.|
|CUU/Epic|1. EPIC Usuario consulta las próximas carreras.<br>2. EPIC Moderador carga información sobre una nueva carrera.<br>3. EPIC Moderador actualiza resultados de una sesión.<br>4. CUU Usuario lee información de una carrera.<br>5. CUU Usuario solicita donde ver una carrera.|

Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Usuario.<br>2. CRUD Blog/Post |
|Listado<br>+<br>detalle|1. Listado de posts, muestra los posts del foro, ordenados por fecha de publicación.
|CUU/Epic|1. CUU Usuario realiza un post en el foro.<br>2. EPIC Moderador elimina un post.<br>3. EPIC Sistema envía una notificación a usuarios cuando una sesión está por comenzar.<br>4. EPIC Sistema envía un post de posible interés a usuario.<br>5. EPIC Moderador elimina un comentario de un post.|
