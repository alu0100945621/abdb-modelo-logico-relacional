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


## 3. Trigger para actualizar el stock (VIVERO)

