# Proyecto de Gestión de Usuarios y Tareas

Este proyecto es una aplicación full-stack que permite gestionar usuarios y tareas asignadas a esos usuarios. La aplicación consta de un backend desarrollado con NestJS y un frontend desarrollado con React.

## Tabla de Contenidos

- [Requisitos](#requisitos)
- [Instalación](#instalación)
  - [Backend](#backend)
  - [Frontend](#frontend)
- [Ejecución](#ejecución)
- [Endpoints de la API](#endpoints-de-la-api)
- [Interfaz Gráfica](#interfaz-gráfica)
- [Contribución](#contribución)
- [Licencia](#licencia)

## Requisitos

- Node.js (versión 14 o superior)
- npm (versión 6 o superior)
- MongoDB (o PostgreSQL)

## Instalación

### Backend

1. **Instalación de NestJS:**

   Primero, instala la CLI de NestJS globalmente:

   ```bash
   npm i -g @nestjs/cli
   ```

2. **Creación del Proyecto:**

   Crea un nuevo proyecto NestJS:

   ```bash
   nest new backend
   cd backend
   ```

3. **Instalación de Dependencias:**

   Instala las dependencias necesarias para MongoDB, TypeORM, y validaciones:

   ```bash
   npm install @nestjs/mongoose mongoose
   npm install @nestjs/typeorm typeorm pg
   npm install class-validator class-transformer
   ```

4. **Generación de Módulos, Controladores y Servicios:**

   Genera los módulos, controladores y servicios necesarios:

   ```bash
   nest generate module users
   nest generate controller users
   nest generate service users

   nest generate module tasks
   nest generate controller tasks
   nest generate service tasks
   ```

5. **Implementación de Usuarios:**

   - **Controlador y Servicio:**

     Implementa el controlador y el servicio en `users/users.controller.ts` y `users/users.service.ts`.

   - **DTOs:**

     Crea un archivo `user.dto.ts` en la carpeta `users/dto` para definir los DTOs.

6. **Implementación de Tareas:**

   - **Controlador y Servicio:**

     Implementa el controlador y el servicio en `tasks/tasks.controller.ts` y `tasks/tasks.service.ts`.

### Frontend

1. **Configuración del Proyecto React:**

   Crea un nuevo proyecto React con TypeScript:

   ```bash
   npx create-react-app frontend --template typescript
   cd frontend
   ```

2. **Instalación de Dependencias:**

   Instala Axios y React Router DOM:

   ```bash
   npm install axios react-router-dom
   ```

3. **Creación de Componentes:**

   Crea los componentes necesarios para listar usuarios, detalles de tareas, y formularios para agregar, editar y eliminar usuarios y tareas.

4. **Creación de Páginas:**

   Crea las páginas necesarias para la lista de usuarios y los detalles de un usuario con sus tareas asignadas.

## Ejecución

1. **Ejecuta el Backend:**

   ```bash
   npm run start
   ```

2. **Ejecuta el Frontend:**

   ```bash
   npm start
   ```

3. **Abre tu Navegador:**

   Navega a `http://localhost:3000` para ver la aplicación en funcionamiento.

## Endpoints de la API

### Usuarios

- `GET /users`: Obtener todos los usuarios.
- `POST /users`: Crear un nuevo usuario.
- `PUT /users/:id`: Actualizar un usuario existente.
- `DELETE /users/:id`: Eliminar un usuario.

### Tareas

- `GET /tasks`: Obtener todas las tareas.
- `POST /tasks`: Crear una nueva tarea.
- `PUT /tasks/:id`: Actualizar una tarea existente.
- `DELETE /tasks/:id`: Eliminar una tarea.

## Interfaz Gráfica

La interfaz gráfica permite:

- Ver una lista de usuarios.
- Ver los detalles de un usuario y las tareas asignadas a ese usuario.
- Agregar, editar y eliminar usuarios y tareas.

## Contribución

Las contribuciones son bienvenidas. Por favor, abre un issue o envía un pull request para cualquier mejora o corrección.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
```

Este `README.md` proporciona una guía completa para la instalación, configuración y ejecución del proyecto, así como una descripción de los endpoints de la API y la interfaz gráfica. También incluye secciones para contribuciones y licencia. Puedes personalizarlo según tus necesidades específicas.
