# 🖥️ **Base Express Typescript Server**

Este proyecto es una estructura básica de un servidor backend utilizando **Express** y **TypeScript**. Incluye configuraciones para **JWT**, **Bcryptjs**, **Morgan**, **Cors**, y **Dotenv**.

## 📁 **Estructura del Proyecto**

```
.env
.gitignore
package.json
README.md
src/
  app.ts
  core/
    middlewares/
      verifyId.middleware.ts
  modules/
    _root/
      _root.controller.ts
      _root.routes.ts
  server.ts
  utils/
    bcrypt.util.ts
    jwt.util.ts
tsconfig.json
```

### 📄 **Archivos y Directorios**

- **.env**: Archivo de configuración de variables de entorno.
- **.gitignore**: Archivo para ignorar directorios y archivos en Git.
- **package.json**: Archivo de configuración de npm, incluye dependencias y scripts.
- **README.md**: Archivo de documentación del proyecto.
- **src/**: Directorio principal del código fuente.
  - **app.ts**: Punto de entrada principal del servidor.
  - **core/middlewares/**: Directorio para middlewares.
    - **verifyId.middleware.ts**: Middleware para verificar el ID en las solicitudes.
  - **modules/_root/**: Directorio para el módulo raíz.
    - **_root.controller.ts**: Controlador para manejar las solicitudes a la ruta raíz.
    - **_root.routes.ts**: Definición de las rutas para el módulo raíz.
  - **server.ts**: Configuración e inicialización del servidor Express.
  - **utils/**: Directorio para utilidades.
    - **bcrypt.util.ts**: Utilidad para manejar el hashing y comparación de contraseñas con Bcrypt.
    - **jwt.util.ts**: Utilidad para manejar la generación y verificación de tokens JWT.
- **tsconfig.json**: Archivo de configuración de TypeScript.

## 📥 **Instalación**

1. Clona el repositorio:
   ```sh
   git clone https://github.com/jebcdev/base-express-typescript-server
   ```
2. Instala las dependencias:
   ```sh
   npm install
   ```

## ⚙️ **Configuración**

Crea un archivo **`.env`** en la raíz del proyecto con el siguiente contenido:

```
API_PREFIX="/api/v1"  # Prefijo de la API, útil para versionar las rutas y tener un punto común.
PORT=4000  # Puerto en el que el servidor estará escuchando.
BCRYPT_SALT=10  # Valor para el "salt" que se usará al hashear las contraseñas con bcrypt.
JWT_SECRET="aVerySecretString"  # Clave secreta para firmar y verificar tokens JWT. Mantenerla segura.
```

## 📦 **Scripts de npm**

- **build**: Compila el proyecto TypeScript.
  ```sh
  npm run build
  ```
- **dev**: Inicia el servidor en modo desarrollo.
  ```sh
  npm run dev
  ```
- **start**: Inicia el servidor en modo producción.
  ```sh
  npm start
  ```

## 🧑‍💻 **Descripción de los Archivos Principales**

### `app.ts`
Este archivo es el punto de entrada principal del servidor. Carga las variables de entorno y crea una instancia de la clase **Server**, iniciando el servidor. 🚀

### `server.ts`
Este archivo configura e inicializa el servidor **Express**. Define los middlewares y las rutas del servidor. ⚙️

### `verifyId.middleware.ts`
Este archivo define un middleware para verificar el ID en las solicitudes. Verifica si el parámetro **id** está presente y si es un número válido. 🔍

### `_root.controller.ts`
Este archivo define el controlador para manejar las solicitudes a la ruta raíz. Responde con un mensaje de bienvenida y detalles de la API. 💬

### `_root.routes.ts`
Este archivo define las rutas para el módulo raíz. Registra la ruta raíz usando el prefijo de la API. 🌍

### `bcrypt.util.ts`
Este archivo define una utilidad para manejar el hashing y comparación de contraseñas utilizando **Bcrypt**. 🔐

### `jwt.util.ts`
Este archivo define una utilidad para manejar la generación y verificación de **tokens JWT**. 🎟️

## 🚀 **Ejecución del Servidor**

Para iniciar el servidor en modo desarrollo, ejecuta:

```sh
npm run dev
```

Para iniciar el servidor en modo producción, ejecuta:

```sh
npm start
```

El servidor estará corriendo en `http://localhost:4000/api/v1`. 🌐

## 🤝 **Contribución**

Si deseas contribuir a este proyecto, eres libre y estas invitado a hacerlo