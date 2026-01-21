# Social Network – Full Stack Project

## Descripción general

Este proyecto consiste en el desarrollo de una **red social tipo Facebook** utilizando un stack moderno y profesional orientado a aplicaciones reales en producción. El objetivo es construir una plataforma con autenticación segura, interacción social (posts, likes, comentarios, seguidores) y una arquitectura escalable.

El proyecto está dividido claramente en **Frontend** y **Backend**, ambos contenidos dentro de una carpeta raíz común para mantener orden, mantenibilidad y buenas prácticas.

---

## Stack tecnológico

### Frontend

* React
* Vite
* React Router DOM
* Context API
* JWT (consumo de autenticación)
* CSS / Tailwind (opcional)

### Backend

* Node.js
* Express
* JWT (autenticación y autorización)
* SQL (PostgreSQL o MySQL)
* bcrypt (hash de contraseñas)
* dotenv
* cors

---

## Estructura del proyecto

```
social-network/
├── client/        # Frontend (React + Vite)
└── server/        # Backend (Node.js + Express + SQL)
```

### Frontend (`/client`)

```
client/
├── public/
├── src/
│   ├── api/            # Llamadas HTTP a la API
│   ├── assets/         # Recursos estáticos
│   ├── components/     # Componentes reutilizables
│   ├── context/        # Contextos globales (Auth)
│   ├── hooks/          # Custom hooks
│   ├── pages/          # Vistas principales
│   ├── routes/         # Rutas protegidas
│   ├── services/       # Lógica de negocio frontend
│   ├── styles/         # Estilos globales
│   ├── utils/          # Funciones helper
│   ├── App.jsx
│   └── main.jsx
├── package.json
└── vite.config.js
```

### Backend (`/server`)

```
server/
├── src/
│   ├── config/         # Configuración (DB, env)
│   ├── controllers/    # Lógica de los endpoints
│   ├── middlewares/    # Middlewares (JWT, errores)
│   ├── models/         # Modelos SQL
│   ├── routes/         # Rutas de la API
│   ├── services/       # Servicios reutilizables
│   ├── utils/          # Helpers
│   ├── app.js          # Configuración de Express
│   └── server.js       # Inicio del servidor
├── package.json
└── .env
```
---

## Scripts de ejecución

### Frontend

```
cd client
npm run dev
```

### Backend

```
cd server
npm run dev
```

---

## Flujo de autenticación (JWT)

1. El usuario se registra o inicia sesión
2. El backend valida credenciales
3. Se genera un JWT
4. El frontend almacena el token
5. Las rutas protegidas validan el JWT
6. El backend autoriza o rechaza la petición

---

## Funcionalidades del MVP

### Autenticación

* Registro de usuario
* Login
* Logout
* Protección de rutas

### Social

* Crear publicaciones
* Feed principal
* Likes
* Comentarios
* Seguir / dejar de seguir usuarios

### Seguridad

* Contraseñas hasheadas
* Middleware JWT
* Validación de permisos

---

## Escalabilidad futura

* WebSockets (chat / notificaciones)
* Redis (caché)
* CDN para imágenes
* Microservicios
* Optimización de consultas SQL

## Autor

**Luis David Gil Cabarcas**

Frontend Developer / Full Stack en formación