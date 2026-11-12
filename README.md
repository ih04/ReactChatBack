# React Chat - Backend

## 📌 Descripción

Backend de una aplicación de chat en tiempo real desarrollada con **Node.js, Express y Socket.IO**, conectada a un frontend creado con React.

El servidor gestiona la conexión entre los usuarios y la comunicación de mensajes en tiempo real mediante WebSockets. El proyecto también contempla el uso de Firebase para el almacenamiento de datos.

## 🚀 Demo
https://poised-charo-frpln-f8bf6475.koyeb.app/

## 🛠️ Tecnologías utilizadas

- **Node.js:** entorno de ejecución de JavaScript en el servidor.
- **Express:** framework para crear el servidor web y gestionar las peticiones HTTP.
- **Socket.IO:** comunicación en tiempo real entre los usuarios mediante eventos y conexiones bidireccionales.
- **Firebase:** servicio previsto para el almacenamiento de datos del proyecto.
- **ES Modules:** sistema de módulos de JavaScript utilizado en el backend.

## ⚙️ Funcionamiento

- El servidor crea una aplicación con Express y un servidor HTTP.
- Socket.IO gestiona las conexiones de los usuarios al chat.
- Cuando un usuario envía un mensaje, el servidor recibe el evento `message`.
- El mensaje se retransmite al resto de usuarios conectados mediante `socket.broadcast.emit()`, sin enviárselo de vuelta al emisor.
- Cada mensaje contiene el texto enviado y un identificador del usuario que lo ha enviado.
- Express permite servir los archivos estáticos del frontend de React desde la carpeta `public`.

## 🚀 Instalación y ejecución

### Requisitos previos

- Node.js y npm instalados.

### Pasos

1. Clonar el repositorio:

   ```bash
   git clone <URL_DEL_REPOSITORIO>
   ```

2. Acceder a la carpeta del backend:

   ```bash
   cd ReactChatBack-master
   ```

3. Instalar las dependencias:

   ```bash
   npm install
   ```

4. Iniciar el servidor en modo desarrollo:

   ```bash
   npm run dev
   ```

   O iniciar el servidor normalmente:

   ```bash
   npm start
   ```

Por defecto, el servidor se ejecuta en el puerto `4000`. Si se define la variable de entorno `PORT`, utilizará el puerto indicado.

## 🔗 Integración con el frontend

Este backend está diseñado para trabajar junto con un frontend desarrollado en React, que se comunica con el servidor mediante Socket.IO para enviar y recibir mensajes en tiempo real.

## 📁 Estructura principal

```text
ReactChatBack/
├── index.js       # Servidor Express y configuración de Socket.IO
├── package.json   # Dependencias y scripts del proyecto
└── README.md      # Documentación del backend
```

## 📄 Scripts disponibles

| Comando | Descripción |
|---|---|
| `npm run dev` | Inicia el servidor con Nodemon para facilitar el desarrollo. |
| `npm start` | Inicia el servidor con Node.js. |
| `npm run build` | Instala las dependencias del frontend y genera su compilación de producción. |

## 🔮 Posibles mejoras

- Integrar el almacenamiento de mensajes en Firebase para conservar el historial del chat.
- Restringir el acceso al servidor mediante una configuración específica de CORS.
- Añadir autenticación de usuarios y gestión de salas de chat.
- Mejorar el manejo de errores y las desconexiones.
