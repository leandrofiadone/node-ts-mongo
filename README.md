
# ts-login-back Boilerplate

Este boilerplate es una configuración básica para un backend en Node.js usando TypeScript. Incluye las dependencias necesarias para trabajar con Express, Mongoose (para MongoDB), y otras herramientas como `nodemon` para el desarrollo.

## Descripción

Este proyecto está diseñado para ser un punto de partida para aplicaciones de backend que requieren autenticación o manejo de datos en una base de datos MongoDB. Utiliza TypeScript para un mejor soporte de tipado estático y una mayor escalabilidad en el desarrollo.

## Estructura del Proyecto

El proyecto tiene la siguiente estructura básica:

```
ts-login-back/
├── dist/           # Archivos compilados de TypeScript
├── src/            # Código fuente en TypeScript
├── .env            # Variables de entorno (se requiere para configuración)
├── package.json    # Dependencias y scripts de Node.js
└── tsconfig.json   # Configuración de TypeScript
```

## Dependencias

El proyecto incluye las siguientes dependencias:

### Dependencias principales:

- `axios`: Cliente HTTP para hacer solicitudes.
- `cors`: Middleware para habilitar CORS (Cross-Origin Resource Sharing).
- `dotenv`: Para cargar variables de entorno desde un archivo `.env`.
- `express`: Framework para crear el servidor y manejar las rutas.
- `mongoose`: ODM (Object Data Modeling) para interactuar con MongoDB.

### Dependencias de desarrollo:

- `@types/cors`: Tipos de TypeScript para `cors`.
- `@types/express`: Tipos de TypeScript para `express`.
- `@types/node`: Tipos de TypeScript para Node.js.
- `nodemon`: Herramienta para reiniciar el servidor automáticamente durante el desarrollo.
- `ts-node`: Ejecutar TypeScript directamente sin necesidad de compilar previamente.
- `typescript`: Compilador de TypeScript.

## Scripts

El archivo `package.json` incluye los siguientes scripts preconfigurados:

- `clean`: Elimina la carpeta `dist`, donde se almacenan los archivos compilados.
- `build`: Ejecuta el script `clean` y luego compila los archivos TypeScript.
- `dev`: Ejecuta `npm run build` y luego inicia el servidor con `nodemon`, que reinicia el servidor automáticamente cuando se detectan cambios en los archivos.
- `start`: Ejecuta `npm run build` y luego inicia el servidor en producción con Node.js.

## Instalación

Para instalar las dependencias del proyecto, ejecuta:

```bash
npm install
```

## Configuración de TypeScript

Este proyecto está configurado para utilizar TypeScript. Asegúrate de tener un archivo `tsconfig.json` en la raíz del proyecto con las siguientes configuraciones mínimas:

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "outDir": "./dist",
    "rootDir": "./src",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "forceConsistentCasingInFileNames": true
  },
  "include": ["src/**/*"],
  "exclude": ["node_modules"]
}
```

## Variables de Entorno

Asegúrate de crear un archivo `.env` en la raíz del proyecto para almacenar tus variables de entorno, como la URL de conexión a la base de datos y las credenciales de autenticación. Un ejemplo de archivo `.env` puede ser:

```
DB_URI=mongodb://localhost:27017/ts-login-back
SECRET_KEY=mysecretkey
```

## Uso

1. Compilar y ejecutar el proyecto en modo desarrollo:

```bash
npm run dev
```

2. Ejecutar el proyecto en producción (después de compilar):

```bash
npm start
```

## Contribución

Si deseas contribuir a este proyecto, por favor abre un issue o envía un pull request.

## Licencia

Este proyecto está bajo la Licencia ISC. Consulta el archivo `LICENSE` para más detalles.