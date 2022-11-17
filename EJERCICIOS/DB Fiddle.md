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

https://www.db-fiddle.com/f/qPV662LxGenZ3HKCJCJPS5/0 - Consultas

# Ejercicio moodle Base de datos tienda informatica

https://www.db-fiddle.com/f/4wTCZtj8UY48Lai8En1AEk/0

USE tienda;

        /*Numero total de productos en la tabla productos*/
        SELECT COUNT (codigo_producto)
        FROM producto;

        /*Numero total de productos de cada fabricante*/
        SELECT nombre_fabrica, COUNT(nombre_producto)
        FROM producto
        LEFT JOIN fabricante ON fabricante.codigo_fabrica=producto.codigo_fabrica1;
        

