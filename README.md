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
  - Accedes a los **productos** en el update del **RestaurantController**
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

# ERRORES COMUNES
  - Si el botón/confirmationModal funciona pero el patch da error y no se puede hacer la función de dicho botón como por ejemplo fijar un restaurante, seguramente en el error esté en la función del controller.
  - Mirar que en el validation se importe el modelo como '../../models/models.js'
  - El findByPK() lleva en los paréntesis esto: (req.params.restaurantId)  y **no** lleva esto: ({ where: { id: req.params.restaurantId } })
  - Pueden no aparecer las cosas en el frontend por no importar el modelo en el controller aunque no salte el error en el visual
  - Si el problema es crear una nueva pantalla de creación de actuaciones por ejemplo, y sale el frontend en blanco probar a comentar el screen de creación para ver si sale bien y los botones tb(aunque no funcionen). A continuación mirar que se importen bien las cosas, por ejemplo no suele notificarse el error pero hace que no se cree la pantalla -->>> import { Pressable, ScrollView, StyleSheet, View } from 'react-native' hay que importar el StyleSheet
  - El navigate a RestaurantsScreen es así navigation.navigate('RestaurantsScreen', { dirty: true }), no hay que pasar ningún ID



