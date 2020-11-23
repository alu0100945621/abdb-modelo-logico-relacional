**Míriam Núñez García**
# Modelo logico relacional

Crear el esquema de la BDD del diseño lógico utilizando el software MySql Workbench correspondiente al modelo conceptual de:

- La empresa de viveros (Carpeta Viveros).

![vivero_workbench](./Catastro/catastro_workbench.png)

- La Base de Datos del Catastro (Carpeta Catastro).

![catastro_workbench](./Viveros/vivero_workbench.png)


# Triggers

## 1. Trigger para crear email (VIVERO)

En primer lugar, creamos el procedimiento *crear_email*.

![crear_email](./Images/crear_email.png)

Después, creamos le trigger que se ejecutará antes de insertar los valores en la tabla *CLIENTE*.

![trigger_email](./Images/trigger_email.png)

Como podemos ver en la siguiente imagen, en las dos primeras filas no se insertó el campo del email, así que se formó automáticamente, mientras que en la tercera, sí que se insertó.

![email](./Images/email.png)


## 2. Trigger para comprobar que una persona no vive en dos viviendas (CATASTRO)

Para comprobar que una persona no pueda tener en la base de datos que vive en un piso y en una vivienda unifamiliar a la vez, utilizamos el siguiente trigger.

Nos encontramos con el caso de insertar una persona nueva:

![insert](./Images/insert.png)

![persona_insert](./Images/persona_insert.png)

Y el caso de actualizar una persona existente:

![update](./Images/update.png)

![persona_update](./Images/persona_update.png)


## 3. Trigger para actualizar el stock (VIVERO)

Para mantener actualizado el stock controlamos las inserciones en la tabla *PRODUCTO_PEDIDO*, ya que si un producto forma parte de un pedido el stock de este disminuirá. Utilizaremos esto para las dos tablas que tienen el atributo *stock*.

![trigger_actualizar](./Images/trigger_actualizar.png)

Como vemos en la diferencia entre las tablas iniciales:

![antes](./Images/antes.png)

Y las tablas que quedan como resultado de insertar valores en la tabla *PRODUCTO_PEDIDO*, los valores disminuyen.

![actualizar_stock](./Images/actualizar_stock.png)
