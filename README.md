# TP FINAL DSW

# 🏎️ descalifica2 🏎️

Repo de entregables y documentación final del proyecto.

### 👥Integrantes

- 52818 \- Barroso Bollero, Agustín
- 52962 \- Taborda, Ignacio
- 52961 \- Figueroa, Francisco Alejandro
- 52847 \- Taborda, Santiago

**Cursado en:** UTN FRRo, Catedra DSW, ISI 303 2025\.

### 💡 Idea del proyecto

Descalifica2 es un sitio web dedicado principalmente a la Fórmula 1, donde podrás consultar el calendario de carreras, acceder a información detallada sobre cada evento y mantenerte al día con las noticias sobre automovilismo. El objetivo del sitio es mantener informada a toda la comunidad interesada en el deporte, brindando las fechas de cada Gran Premio, dónde verlo en vivo, y datos sobre las escuderías participantes junto a sus pilotos, como los resultados de las carreras o el torneo. Los usuarios pueden crear un perfil personalizado, indicando su nombre, escuderías, circuitos y pilotos favoritos para adaptar su experiencia en la plataforma. Además, podrán participar en un foro donde intercambiar opiniones, debatir y compartir ideas con otros fanáticos de la Fórmula 1\.

### 📝 Descripción

**Descalifica2** está dividido en dos repositorios independientes, ambos en **TypeScript** y gestionados con **pnpm**: un **backend** (`descalifica2-back`) que expone una API REST y un **frontend** (`descalifica2-front`) que la consume.

El **backend** usa **Node.js + Express** y **MikroORM** sobre **MySQL**. Está organizado por **vertical slicing**: dentro de `src/` cada entidad tiene su propia carpeta con su `entity`, `controller` y `routes`. Todo lo que no es del dominio está separado en dos carpetas. `src/services/` con las integraciones (como la API de OpenF1, un bot de Telegram, Google OAuth, entre otros). `src/shared/` configs y **Swagger**, disponible en `/api/docs`. La autenticación usa JWT y bcrypt. El punto de entrada es `app.ts`, que registra todas las rutas bajo `/api/*`. Está deployeada en Railway.

El **frontend** es una SPA hecha con **React** y compilada **Vite** y estilada con **shadcn/ui** (la cual implementa **Tailwind CSS**), deployeada en Vercel. Las rutas se manejan con React Router, y algunas están protegidas por componentes que solo dejan entrar a usuarios autenticados o administradores. El enfoque es mobile-first los estilos base están pensados para pantallas chicas y se amplían, así que la interfaz se adapta bien desde el celular hasta el escritorio. Toda la comunicación con el backend se realiza a través Axios. Se usa un interceptor para agregar el token JWT a cada petición. El frontend también se integra con Google OAuth para iniciar sesión, con OpenF1 (a través del backend) para resultados, y con un bot de Telegram para notificaciones.

## ℹ️ Más información del proyecto

- **Índice de la documentación:** [docs/README.md](https://github.com/GupCus/tpDSW/blob/main/docs/README.md)
- **Nuestro proposal:** [/proposal.md](https://github.com/GupCus/tp/blob/main/proposal.md)
- **Repo front:** [descalifica2-front](https://github.com/GupCus/descalifica2-front)
- **Repo back:** [descalifica2-back](https://github.com/GupCus/descalifica2-back)
