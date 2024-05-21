# Restaurantes SPA

Este repositorio contiene una Single Page Application (SPA) para la gestión de restaurantes, que incluye tanto el backend como el frontend. La aplicación permite a los dueños de restaurantes gestionar la información de sus establecimientos.

## Estructura del Proyecto

El proyecto está organizado en varias carpetas, cada una con responsabilidades específicas.

### Seeders

- **Descripción**: Se utilizan para poblar la base de datos con datos iniciales o de prueba.
- **Uso**: Archivos que crean registros de ejemplo para restaurantes, menús y dueños de restaurantes.
- **Ejemplo**: Un seeder puede insertar un conjunto de restaurantes iniciales con nombres, ubicaciones y detalles básicos.

### Orders

- **Descripción**: Maneja la lógica relacionada con la gestión de pedidos en los restaurantes.
- **Uso**: Contiene modelos y controladores que gestionan la creación, actualización y seguimiento de pedidos.
- **Ejemplo**: Un archivo en esta carpeta define cómo se crea un nuevo pedido y se actualiza su estado.

### Migrations

- **Descripción**: Manejan los cambios en la estructura de la base de datos a lo largo del tiempo.
- **Uso**: Definen cómo crear y modificar tablas en la base de datos para almacenar datos de restaurantes, menús y usuarios.
- **Ejemplo**: Una migración puede crear una tabla `restaurants` con columnas como `id`, `name`, `address`, y `owner_id`.

### Controller

- **Descripción**: Manejan las solicitudes entrantes, procesan la lógica de negocio y devuelven las respuestas adecuadas.
- **Uso**: Controladores para gestionar las operaciones CRUD de restaurantes y menús.
- **Ejemplo**: Un `RestaurantController` con métodos como `createRestaurant`, `getRestaurant`, `updateRestaurant`, y `deleteRestaurant`.

### Validation

- **Descripción**: Aseguran que los datos entrantes cumplan con ciertos criterios antes de ser procesados por los controladores.
- **Uso**: Reglas para validar datos como el nombre del restaurante, dirección y horarios.
- **Ejemplo**: Un archivo de validación puede comprobar que el nombre del restaurante no esté vacío y que la dirección tenga un formato válido.

### Middleware

- **Descripción**: Funciones que se ejecutan antes o después de las solicitudes a los controladores, utilizadas para tareas como autenticación y autorización.
- **Uso**: Middleware para verificar si el usuario está autenticado y tiene permisos de dueño de restaurante.
- **Ejemplo**: Un `authMiddleware` que comprueba si el usuario ha iniciado sesión y tiene el rol de "owner".

### Routes

- **Descripción**: Definen los endpoints de la API y especifican qué controlador y método deben manejar cada solicitud.
- **Uso**: Configuración de rutas para las operaciones CRUD relacionadas con restaurantes, menús y pedidos.
- **Ejemplo**: Una ruta `/api/restaurants` que maneja solicitudes GET para listar restaurantes, POST para crear uno nuevo, PUT para actualizar un restaurante existente y DELETE para eliminar uno.

```javascript
// routes/restaurantRoutes.js
const express = require('express');
const router = express.Router();
const RestaurantController = require('../controllers/RestaurantController');
const authMiddleware = require('../middleware/authMiddleware');

router.get('/', authMiddleware, RestaurantController.getRestaurants);
router.post('/', authMiddleware, RestaurantController.createRestaurant);
router.put('/:id', authMiddleware, RestaurantController.updateRestaurant);
router.delete('/:id', authMiddleware, RestaurantController.deleteRestaurant);

module.exports = router;
