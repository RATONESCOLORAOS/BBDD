
## CREACIÓN BBDD

- **Motivo**
Esta base de datos fue creada para implementar funcionalidades estadísticas en nuestro proyecto. Permite comparar y guardar datos interesantes de los usuarios de nuestra APP, facilitando la futura implementación de bases estadísticas.

- **Necesidades**

-Versión de MySQL 8.4.0 o superior.  
-MySQL Workbrench (Recomendado).

- **Instalación**

En primer lugar deberás ir a:
 [`transformacion_productos_categoria`](https://github.com/RATONESCOLORAOS/ETL/tree/main/Data/src), para poder crear la tabla productos_categoría y la tabla fuel. 
 En segundo lugar, debes dirigirte al repositorio de BBDD donde encontrarás:  [`query_bbdd`](https://github.com/RATONESCOLORAOS/BBDD), con las consultas SQL necesarias para crear las tablas que faltan.

 - **Estructura**
USER
 -
  PK(id_user)
  Esta tabla recopila toda la información del login del usuario.

  USER LIST 
  -
  PK(id_user_list)
  FK(id_user)
  Esta tabla recopila la información sobre la elección de compra del usuario. 

 COMPARATIVA
 -
 PK(id_comp)
 FK(id_user_list)
 Esta tabla recopila la información que el usuario decidió no elegir en su lista. 

 USER_LIST_PRODUCT
 - 
 PK (id_user, id_producto, id_user_list)
 FK(id_user,id_producto, id_user_list)
 Esta tabla la utilizamos para normalizar la relación de muchos a muchos.
