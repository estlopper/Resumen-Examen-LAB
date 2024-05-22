# Backend

### Seeders

- **Descripción**: Se utilizan para poblar la base de datos con datos iniciales o de prueba.
- **Casos**
    - No es necesario modificar los seeders si se pone un valor por defecto al nuevo atributo en el order.

### Models

- **Descripción**: Donde se crean los datos que irán en la base de datos siguiendo el diagrama de clases .
- **Casos**
    - Si hay que añadir algún atributo nuevo hay que modificar el modelo correspondiente.

### Migrations

- **Descripción**: Definen cómo crear y modificar tablas en la base de datos para almacenar datos.
- **Casos**
    - Si hay que añadir algún atributo nuevo hay que modificar la migración correspondiente.

### Controller

- **Descripción**: Manejan las solicitudes entrantes, procesan la lógica de negocio y devuelven las respuestas adecuadas. Gestionan las operaciones CRUD. 
- **Casos**
    - En el simulacro es una const promote = async function (req, res) que modifica el valor del atributo de promoción.
    - Otro caso sería añadir una operación de create.    

### Validation

- **Descripción**: Aseguran que los **datos entrantes** cumplan con ciertos criterios antes de ser procesados por los controladores. Reglas de validación.
- En el simulacro se añade un nuevo check al que se le pasa una función y comprueba que solo haya un restaurante promocionado del mismo dueño.

### Middleware

- **Descripción**: Funciones que se ejecutan antes o después de las solicitudes a los controladores, utilizadas para tareas como autenticación y autorización.
- En el simulacro no se usa.

### Routes

- **Descripción**: Definen los **endpoints** de la API y especifican qué controlador y método deben manejar cada solicitud. Configuración de las operaciones CRUD.
- **Casos**
    - En el simulacro se crea una nueva ruta app.route('/restaurants/:restaurantId/promote') y se comprueban las correspondientes restricciones.
    - Si creo una nueva función en el controller como puede ser create, tengo que llamarla con .post(RestaurantCategoryController.create)


# Frontend

### Endpoints

- **Descripción**: Donde se obtiene la información del backend
- **Casos**
    - /api/restaurantes
    - Si creo un create en el controller llamo al post aquí
 
### Stack

- **Descripción**: Donde se 'enlazan' dos screens para poder navegar entre ellas




