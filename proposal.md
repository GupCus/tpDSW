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

![Imagen del modelo](https://github.com/GupCus/tp/blob/main/MD%20Descalifica2.drawio.png?raw=true)

## Alcance Funcional

### Alcance Mínimo

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Circuito<br>2. CRUD Escudería<br>3. CRUD Temporada<br>4. CRUD Categoría<br>5. CRUD Piloto|
|CRUD dependiente|1. CRUD Carrera {depende de} CRUD Circuito<br>|
|Listado<br>+<br>detalle| 1. Listado de pilotos, puede ser filtrado por escudería. Muestra nombre completo del piloto y su foto => detalle muestra todos los datos del circuito <br> 2. Listado de circuitos, puede ser filtrado por continente o por tipo de circuito. Muestra nombre del circuito y su trazado => detalle muestra todos los datos del circuito.<br>3. Listado de temporada, muestra todas las carreras (grandes premios) agendadas de una temporada ⇒ detalle muestra todos los detalles de una carrera.|
|CUU/Epic|1. Usuario revisa el calendario actual.<br>2. Usuario mira todas las escuderías.<br>3. Usuario revisa información de un piloto.|

Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Usuario.<br>2. CRUD Post.|
|Listado<br>+<br>detalle|1. Listado de posts, muestra los posts del foro, ordenados por fecha de publicación.
|CUU/Epic|1. Usuario realiza un post en el foro.<br>2. Usuario comenta en un post de otro usuario.|
