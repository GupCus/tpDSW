# Instrucciones de Instalación y Ejecución

A continuación se detalla el paso a paso para poder levantar el proyecto de forma local, tanto el backend como el frontend.

## Prerrequisitos

Para poder correr este proyecto es necesario tener instalado:

- **Node.js** (versión indicada en `.node-version`).
- **fnm** para administrar la versión de node.
- **pnpm** como gestor de paquetes.
- **MySQL** 8.0+

---

## 1\. Backend

1. **Ubicarse en el directorio del backend:**
   Desde la raíz del proyecto, ingresa a la carpeta del backend.

   ```bash
   cd descalifica2-back
   ```

2. **Usar la versión de node del proyecto:**

   ```bash
   fnm use --install-if-missing
   ```

3. **Variables de Entorno:**
   Copia el archivo de ejemplo para crear tus variables de entorno locales (en CMD usar `copy`).

   ```bash
   cp exampleenv.txt .env
   ```

   Completa el `.env`:

   ```env
   PORT=3000
   BDLOCATION=mysql://dsw:dsw@localhost:3306/descalifica2
   JWT_SECRET=una_clave_secreta
   EXPIRA_TOKEN=7d
   FRONTEND_URL=http://localhost:5173
   GOOGLE_KEY=
   TELEGRAM_BOT=
   BREVO_API_KEY=
   EMAIL_FROM=
   ```

   - `GOOGLE_KEY`: crear un ID de cliente OAuth 2.0 (aplicación web) con `http://localhost:5173` como origen autorizado. [Más info](https://developers.google.com/identity/gsi/web/guides/get-google-api-clientid?hl=es-419).
   - `TELEGRAM_BOT`: crear un bot y copiar su token. [Guía oficial de Telegram](https://core.telegram.org/bots/tutorial). En desarrollo el bot no se inicia, así que alcanza con cualquier valor.
   - `BREVO_API_KEY` y `EMAIL_FROM`: crear una API key en [Brevo](https://www.brevo.com/) para el envío de mails.

4. **Instalar dependencias:**

   ```bash
   pnpm install
   ```

5. **Crear el usuario de MySQL e importar el dump de la base de datos:**
   Ejecutar en orden los scripts dentro de [/dumpsbd](../dumpsbd): primero `creacion-usuario.sql` (crea la base y el usuario `dsw`/`dsw`) y luego `dumpbd.sql`.

   **o si deseas no importar la base de datos**
   dentro de MySQL, crear la base y el usuario con los datos que ingresaste en `BDLOCATION` (las tablas se generan solas al iniciar):

   ```sql
   CREATE DATABASE IF NOT EXISTS descalifica2;
   CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
   GRANT ALL PRIVILEGES ON descalifica2.* TO 'username'@'localhost';
   FLUSH PRIVILEGES;
   ```

6. **Ejecutar el proyecto en desarrollo:**

   ```bash
   pnpm start:dev
   ```

   La API queda en `http://localhost:3000/api` y su documentación en `http://localhost:3000/api/docs`.

---

## 2\. Frontend

1. **Ubicarse en el directorio del frontend:**
   Desde la raíz del proyecto, abre otra terminal e ingresa a la carpeta del frontend.

   ```bash
   cd descalifica2-front
   ```

2. **Usar la versión de node del proyecto:**

   ```bash
   fnm use --install-if-missing
   ```

3. **Variables de Entorno:**
   Crea un archivo `.env` con:

   ```env
   VITE_API_URL=http://localhost:3000/api
   VITE_GOOGLE_KEY=
   ```

   `VITE_GOOGLE_KEY` es el mismo ID de cliente usado en `GOOGLE_KEY` del backend.

4. **Instalar dependencias:**

   ```bash
   pnpm install
   ```

5. **Ejecutar el proyecto en desarrollo:**

   ```bash
   pnpm dev
   ```

   La app queda disponible en `http://localhost:5173`.

---

## Problemas comunes

- **"Te falta el env o lo tenes incompleto":** revisar que el `.env` del backend tenga todas las variables del paso 3.
- **"node no es un comando reconocido":** verificar que fnm esté configurado en la terminal desde la que se abre el editor.
- **Error de conexión a la base de datos:** confirmar que MySQL esté corriendo y que el usuario, la contraseña y el nombre de la base coincidan con `BDLOCATION`.
