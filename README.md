- Online Offline:    https://github.com/estlopper/Examen-OnlineOffline.git
  - **Boton** para alternar estados y middleware para comprobar regla general
-
- Promocion Descuento:    https://github.com/estlopper/Examen-PromocionDescuento.git
  - El restaurante tiene un descuento y se aplica a los productos promocionados
  - Se pueden promocionar/despromocionar productos con un **boton**
-
- Promocion:    https://github.com/estlopper/Examen-Promocion.git
  - Promocionar desde creación con un **switch** pero solo puede haber uno promocionado 
  - **Ordenados** por promoción (Mirar en solucion del profesor)
  - **Botón** para alternar promocionado
-
- Nuevas Categorias:    https://github.com/estlopper/Nuevas-Categorias.git
  - Nueva **screen** de creación de categoría
  - Se añade el route en la screen
-
- Ordenados Por Precio:    https://github.com/IISSI2-IS-2022-2023/Parciales/tree/sortProductsByPriceSolution
  - **Botón** para **ordenar** por defecto o para ordenar por precio
-
- Codigos de descuento:    https://github.com/IISSI2-IS-2022-2023/Parciales/tree/restaurantDiscountCodes
  - Se pueden crear un codigo y un descuento desde la pantalla de creacion
  - Este codigo aparece en el titulo del restaurante
-
- Descuento +- 0.5%:    https://github.com/estlopper/Descuentos.git
  - En el edit **formik**, aparecen **dos botones**, uno para incrementar y otro para decrementar un porcentaje
  - Después del save el porcentaje se debe de **aplicar**
  - Debe aparecer un texto en aquellos donde se haya aplicado el porcentaje
  - Confirmation **Modal en un formik**
  - Se modifica el update del controller
-
- Pinned:    https://github.com/estlopper/Pinned.git
  - Se pueden fijar restaurantes desde la creación con un **switch** o desde un botón
  - Los restaurantes fijados aparecerán arriba, **ordenados**
- 
- Visibilidad:    https://github.com/estlopper/Visibilidad.git
  - Se trabaja con diferencias entre fechas y redondeo de las fechas
  - Fecha en formik
  - Uso de **[Sequelize.Op....]**
-
- https://github.com/IISSI2-IS-2024/proyecto-de-curso-xwg5759.git
- https://github.com/IISSI2-IS-2024/Simulacro-Examen.git
- https://github.com/IISSI2-IS-2022-2023/Parciales.git
- https://github.com/IISSI2-IS-2024/Soluciones-examen-junio-2024.git
- 
- https://sequelize.org/master/manual/getting-started.html

- Restaurantes Económicos:    https://github.com/estlopper/Restaurantes-Economicos
- 
- Mejoras de Ecosistema:    https://github.com/estlopper/Mejoras-de-Ecosistema.git
  - Se añade un retardo de 650 ms
  - Se añade un texto aleatorio que puede variar entre 5 opciones
  - Se añade un botón para cambiar de color y otro para cambiar de tamaño de fuente
  - Se añade el botón de mostrar/ocultar contraseña
-
- Mensaje para fans:    https://github.com/estlopper/Mensaje-para-fans.git
  - Se añade un texto que cambia de color cada segundo
  - El texto no ocupará espacio si no existe



const primerDestacado = await Product.findOne({ where: { destacado: true }, order: [['createdAt', 'ASC']] })


# Backend

### Seeders

- **Descripción**: Se utilizan para poblar la base de datos con datos iniciales o de prueba.
- **Casos**
    - No es necesario modificar los seeders si se pone un valor por defecto al nuevo atributo en el model.

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
  - GET: Recuperar datos del servidor.
  - POST: Enviar datos al servidor para crear un nuevo recurso.
  - PUT: Enviar datos al servidor para actualizar un recurso existente, reemplazando su contenido por completo.
  - PATCH: Actualizar parcialmente un recurso existente. Se usa cuando solo necesitas modificar una parte del recurso en lugar de reemplazarlo completamente.


# Frontend

### Endpoints

- **Descripción**: Donde se obtiene la información del backend
- **Casos**
    - /api/restaurantes
    - Si creo un create en el controller llamo al post aquí
 
### Stack

- **Descripción**: Donde se 'enlazan' dos screens para poder navegar entre ellas




