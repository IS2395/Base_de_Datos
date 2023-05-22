# Base de datos biblioteca

https://www.db-fiddle.com/f/umEMiHGa4VmwR7Mvpf8M6Z/0
    
# Base de datos editorial

![Imagen1](https://user-images.githubusercontent.com/111446113/201251841-07b318a1-c3ab-4974-a3c2-56629b18402a.png)


https://www.db-fiddle.com/f/2VvT9JW4mFuUHwpAJF3QzH/1  -  Estructura completa

# Base de datos tienda

https://www.db-fiddle.com/f/tfg8VkdD8MqnHksHivtg9P/1 - Con Querys

https://www.db-fiddle.com/f/tfg8VkdD8MqnHksHivtg9P/2 - Querys de group by y order by

https://www.db-fiddle.com/f/tfg8VkdD8MqnHksHivtg9P/3 - Con IVA

https://www.db-fiddle.com/f/tfg8VkdD8MqnHksHivtg9P/4 - Con ventas

https://www.db-fiddle.com/f/buSdkkAbV3v8e88PhQrnuP/0 - Repaso

https://www.db-fiddle.com/f/igVHQyNSzTPtzk51bJnj2X/0 - Triggers

        Incrementar columna
        UPDATE producto AS i1
        JOIN (
          SELECT clave_prod, @n := @n + 1 AS precio
          FROM producto
          CROSS JOIN (SELECT @n := (SELECT MAX(precio) FROM producto)) AS v
          WHERE precio IS NULL
          ORDER BY clave_prod
        ) AS i2 ON i1.clave_prod = i2.clave_prod
        SET i1.precio = i2.precio;

https://www.db-fiddle.com/f/qPV662LxGenZ3HKCJCJPS5/0 - Consultas

# Ejercicios moodle

https://www.db-fiddle.com/f/4wTCZtj8UY48Lai8En1AEk/0 - 6. Creación de una Base de Datos

https://www.db-fiddle.com/f/4wTCZtj8UY48Lai8En1AEk/1 - 7. Funciones en SQL

https://www.db-fiddle.com/f/eQZ3FBhXE3knmizPH6BuGE/0 - 8. Disparadores

https://www.db-fiddle.com/f/4wTCZtj8UY48Lai8En1AEk/2 - 9. Operaciones en una base de datos

https://www.db-fiddle.com/f/rzWRTWr8qNfdijHVzkME4y/0 - Completo
