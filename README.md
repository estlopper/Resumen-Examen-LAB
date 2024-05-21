# Backend

### Seeders

- **Descripción**: Se utilizan para poblar la base de datos con datos iniciales o de prueba.
- **Uso**: Archivos que crean registros de ejemplo para restaurantes, menús y dueños de restaurantes.
- No es necesario modificar los seeders si se pone un valor por defecto al nuevo atributo en el order.

### Models

- **Descripción**: Donde se crean los datos que irán en la base de datos siguiendo el diagrama de clases .
- Si hay que añadir algún atributo nuevo hay que modificar el modelo correspondiente.

### Migrations

- **Descripción**: Manejan los cambios en la estructura de la base de datos a lo largo del tiempo.
- **Uso**: Definen cómo crear y modificar tablas en la base de datos para almacenar datos de restaurantes, menús y usuarios.
- Si hay que añadir algún atributo nuevo hay que modificar la migración correspondiente.

### Controller

- **Descripción**: Manejan las solicitudes entrantes, procesan la lógica de negocio y devuelven las respuestas adecuadas.
- **Uso**: Controladores para gestionar las operaciones CRUD.
- En el simulacro es una const promote = async function (req, res) que modifica el valor del atributo de promoción.

### Validation

- **Descripción**: Aseguran que los **datos entrantes** cumplan con ciertos criterios antes de ser procesados por los controladores.
- **Uso**: Reglas para validar datos como el nombre del restaurante, dirección, etc.
- En el simulacro se añade un nuevo check al que se le pasa una función y comprueba que solo haya un restaurante promocionado del mismo dueño.

### Middleware

- **Descripción**: Funciones que se ejecutan antes o después de las solicitudes a los controladores, utilizadas para tareas como autenticación y autorización.
- **Uso**: Middleware para verificar si el usuario está autenticado y tiene permisos de dueño de restaurante.
- En el simulacro no se usa.

### Routes

- **Descripción**: Definen los **endpoints** de la API y especifican qué controlador y método deben manejar cada solicitud.
- **Uso**: Configuración de rutas para las operaciones CRUD relacionadas con restaurantes, menús y pedidos.
- En el simulacro se crea una nueva ruta app.route('/restaurants/:restaurantId/promote') y se comprueban las correspondientes restricciones.

