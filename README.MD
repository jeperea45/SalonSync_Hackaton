# Desafío Full Stack: Construyendo Aplicaciones con MERN y PostgreSQL

## Descripción

Este proyecto fue desarrollado durante una hackatón de 3 días con el objetivo de construir una aplicación Full Stack utilizando las tecnologías MERN (MongoDB, Express, React, Node.js) y PostgreSQL. La aplicación permite gestionar proyectos y actividades asociadas.

## Funcionalidades

1. **Gestión de Proyectos**:
   - Agregar nuevos proyectos.
   - Listar proyectos existentes desde MongoDB.
2. **Gestión de Actividades**:
   - Relacionar actividades con proyectos almacenados en PostgreSQL.
   - Listar actividades asociadas a un proyecto.
   - Agregar nuevas actividades para un proyecto específico.
3. **Interfaz de Usuario**:
   - Formularios para agregar proyectos y actividades.
   - Visualización de proyectos y actividades relacionadas.

## Tecnologías Utilizadas

- **Frontend**:
  - React.js
  - React Hook Form
  - Tailwind CSS
  - React-Toastify
- **Backend**:
  - Node.js y Express.js
  - Nodemailer
  - JSON Web Token (JWT)
- **Bases de Datos**:
  - MongoDB para almacenar proyectos.
  - PostgreSQL para almacenar actividades.
- **Herramientas Adicionales**:
  - GitHub para control de versiones.

## Requisitos de Instalación

1. Node.js y npm instalados.
2. MongoDB y PostgreSQL configurados.
3. Clonar el repositorio:
   ```bash
   git clone https://github.com/jeperea45/SalonSync_Hackaton
   cd SalonSync_Hackaton
   ```
4. Instalar dependencias:
   ```bash
   npm install
   ```

## Configuración

1. Configurar las conexiones a MongoDB y PostgreSQL en el archivo `.env`:

   ```
   MONGO_URI=mongodb://localhost:27017/<nombre_base_datos>
   POSTGRES_URI=postgresql://<usuario>:<contraseña>@localhost/<nombre_base_datos>
   JWT_SECRET=<clave_secreta_para_jsonwebtoken>
   SMTP_HOST=<host_smtp_para_nodemailer>
   SMTP_PORT=<puerto_smtp>
   SMTP_USER=<usuario_smtp>
   SMTP_PASS=<contraseña_smtp>
   ```

2. Inicializar las bases de datos:
   - Para MongoDB, crear una colección llamada `proyectos`.
   - Para PostgreSQL, crear las tablas `proyectos` y `actividades` con las relaciones correspondientes.

## Ejecución

1. Iniciar el servidor backend:
   ```bash
   npm run start
   ```
2. Iniciar la aplicación frontend:
   ```bash
   cd client
   npm start
   ```

## Estructura del Proyecto

```
Hackaton-RETO-2
├── backend
│   ├── configuration
│   │   └── BD.js
│   ├── Controller
│   │   ├── controllerAdmin.js
│   │   ├── controllerAuth.js
│   │   ├── controllerReserva.js
│   │   ├── controllerSala.js
│   │   ├── controllerUser.js
│   │   └── Formulario_reserva.js
│   ├── middleware
│   │   └── authMiddleware.js
│   ├── Models
│   │   ├── FormularioReservacion.js
│   │   ├── Reserva.js
│   │   ├── Room.js
│   │   ├── Sala.js
│   │   └── User.js
│   ├── paneles
│   │   ├── admin.js
│   │   └── user.js
│   ├── Routes
│   │   ├── adminRoutes.js
│   │   ├── authRoutes.js
│   │   ├── FormularioReservacion.js
│   │   ├── routeReserva.js
│   │   ├── routeSala.js
│   │   └── usuarioRoutes.js
│   ├── .env
│   ├── .gitignore
│   ├── bd.sql
│   ├── json.sql
│   ├── package-lock.json
│   ├── package.json
│   └── servidor.js
├── frontend
│   ├── public
│   │   └── vite.svg
│   ├── src
│   │   ├── api
│   │   │   └── auth.js
│   │   ├── assets
│   │   │   └── react.svg
│   │   ├── components
│   │   │   ├── CardAdmin.jsx
│   │   │   ├── Error.jsx
│   │   │   ├── Footer.jsx
│   │   │   └── Header.jsx
│   │   ├── context
│   │   │   ├── AuthContext.jsx
│   │   │   └── ReservationsContext.jsx
│   │   ├── hooks
│   │   │   ├── useAuth.jsx
│   │   │   └── useReservations.jsx
│   │   ├── pages
│   │   │   ├── AdminDashboard.jsx
│   │   │   ├── Error404.jsx
│   │   │   ├── Home.jsx
│   │   │   ├── ListRervations.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   └── UserDashboard.jsx
│   │   ├── App.jsx
│   │   ├── index.css
│   │   └── main.jsx
│   ├── .gitignore
│   ├── eslint.config.js
│   ├── index.html
│   ├── package-lock.json
│   ├── package.json
│   ├── postcss.config.js
│   ├── README.md
│   ├── tailwind.config.js
│   └── vite.config.js
```

## Endpoints de la API

### Proyectos

- **POST** `/api/proyectos`: Agregar un nuevo proyecto.
- **GET** `/api/proyectos`: Obtener todos los proyectos.

### Actividades

- **POST** `/api/actividades`: Agregar una nueva actividad.
- **GET** `/api/actividades/:proyectoId`: Obtener actividades relacionadas con un proyecto.

## Aprendizajes Clave

- Integración de bases de datos relacionales y no relacionales.
- Diseño de APIs RESTful.
- Consumo de datos en React.js desde un backend en Node.js.
- Configuración y manejo de bases de datos con MongoDB y PostgreSQL.

## Equipo

- [Santiago Duque @Santid21]
- [Kevin Gaviria @Kevingo98]
- [Alvaro Jose Ibarra Fernandez @AlvaroJose1357]
- [Juan Esteban Perea Olivares @jeperea45]
- [Jose Alejandro Velez Sanabria @ch3p3l1t0]
