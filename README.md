## Creación de la Base de Datos

### Motivo
Esta base de datos se creó para implementar funcionalidades estadísticas en nuestro proyecto. Permite comparar y almacenar datos relevantes de los usuarios de nuestra aplicación, facilitando futuras implementaciones de análisis estadísticos.

### Necesidades

- Versión de MySQL 8.4.0 o superior.
- MySQL Workbench (recomendado).

### Instalación

1. Primero, visita el repositorio [`transformacion_productos_categoria`](https://github.com/RATONESCOLORAOS/ETL/tree/main/Data/src) para crear las tablas `productos_categoría` y `fuel`.
   
2. Luego, dirígete al repositorio de la base de datos [`BBDD`](https://github.com/RATONESCOLORAOS/BBDD), donde encontrarás las consultas SQL necesarias para crear las demás tablas.

### Estructura de la Base de Datos

- **USER**
  - PK(id_user): Tabla que recopila la información del inicio de sesión del usuario.

- **USER_LIST**
  - PK(id_user_list)
  - FK(id_user): Tabla que recoge la información sobre las elecciones de compra del usuario.

- **COMPARATIVA**
  - PK(id_comp)
  - FK(id_user_list): Tabla que almacena la información de los productos que el usuario decidió no elegir en su lista.

- **USER_LIST_PRODUCT**
  - PK(id_user, id_producto, id_user_list)
  - FK(id_user, id_producto, id_user_list): Tabla utilizada para normalizar la relación de muchos a muchos.


