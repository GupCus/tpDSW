# Instrucciones de Instalación y Ejecución

A continuación se detalla el paso a paso para poder levantar el proyecto de forma local, tanto el backend como el frontend.

## Prerrequisitos

Para poder correr este proyecto es necesario tener instalado:

- **Node.js**.
- **pnpm** como gestor de paquetes. También puede usarse **npm**.
- **fnm** para administrar la versión de node.
- **MySQL** 8.0+

---

## 1. Backend

1. **Ubicarse en el directorio del backend:**
   Desde la raíz del proyecto, ingresa a la carpeta del backend.

   ```bash
   cd descalifica2-back
   ```

2. **Instalar la versión de node:**

   ```bash
   fnm use
   ```

3. **Variables de Entorno:**
   Copia el archivo de ejemplo para crear tus variables de entorno locales.

   ```bash
   cp exampleenv.txt .env
   ```

   - Generar una clave de Oauth 2.0, [más info](https://docs.cloud.google.com/docs/authentication/api-keys?hl=es-419).
   - Generar un bot y su respectiva clave. [Guía oficial de Telegram](https://core.telegram.org/bots/tutorial).
   - Elegir un servicio de email y completar las respectivas variables.

4. **Instalar dependencias:**

   ```bash
   pnpm install
   ```

5. **Crear el usuario de MySQL**
   dentro de MySQL, crear el usuario con la contraseña que ingresamos en el env:

   ```sql
   CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
   GRANT ALL PRIVILEGES ON descalifica2.* TO 'username'@'localhost' IDENTIFIED BY 'password';
   FLUSH PRIVILEGES;
   ```

6. **Ejecutar el proyecto en desarrollo:**
   ```bash
   pnpm start:dev
   ```

---

## 2. Frontend

1. **Ubicarse en el directorio del frontend:**
   Desde la raíz del proyecto, abre otra terminal e ingresa a la carpeta del frontend.

   ```bash
   cd descalifica2-front
   ```

2. **Variables de Entorno:**
   crear un .env y completar las variables para que apunte correctamente al backend.

3. **Instalar dependencias:**

   ```bash
   pnpm install
   ```

4. **Ejecutar el proyecto en desarrollo:**
   ```bash
   pnpm vite
   ```
