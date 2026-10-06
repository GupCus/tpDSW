# Instrucciones de Instalación y Ejecución

A continuación se detalla el paso a paso para poder levantar el proyecto de forma local, tanto el backend como el frontend.

## Prerrequisitos

Para poder correr este proyecto es necesario tener instalado:
- **Node.js** (versión recomendada LTS).
- **pnpm** como gestor de paquetes.

---

## 1. Backend

1. **Ubicarse en el directorio del backend:**
   Desde la raíz del proyecto, ingresa a la carpeta del backend.
   ```bash
   cd descalifica2-back
   ```

2. **Variables de Entorno:**
   Copia el archivo de ejemplo para crear tus variables de entorno locales.
   ```bash
   cp exampleenv.txt .env
   ```
   *(Asegúrate de configurar correctamente las variables dentro del archivo `.env` según tu entorno de base de datos).*

3. **Instalar dependencias:**
   ```bash
   pnpm install
   ```

4. **Ejecutar el proyecto en desarrollo:**
   ```bash
   pnpm run dev
   ```
   *(Dependiendo de los scripts de tu `package.json`, podría ser `pnpm run start:dev`)*

---

## 2. Frontend

1. **Ubicarse en el directorio del frontend:**
   Desde la raíz del proyecto, abre otra terminal e ingresa a la carpeta del frontend.
   ```bash
   cd descalifica2-front
   ```

2. **Variables de Entorno:**
   Si existe un archivo `.env.example`, cópialo a `.env`.
   ```bash
   cp .env.example .env
   ```
   *(O asegúrate de configurar las variables necesarias para apuntar al puerto donde corre el backend).*

3. **Instalar dependencias:**
   ```bash
   pnpm install
   ```

4. **Ejecutar el proyecto en desarrollo:**
   ```bash
   pnpm run dev
   ```

Con ambos servicios corriendo, la aplicación completa estará disponible de forma local.
