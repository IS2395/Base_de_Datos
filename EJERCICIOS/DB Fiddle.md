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
    UPDATE producto
    JOIN (
      SELECT nom_prod, @n := @n + 1 AS clave_prod
      FROM producto
      CROSS JOIN (SELECT @n := (SELECT MAX(clave_prod) FROM producto)) AS v
      WHERE clave_prod IS NULL
      ORDER BY clave_prod
    ) AS producto2 ON producto.nom_prod = producto2.nom_prod
    SET producto.clave_prod = producto2.clave_prod;

    CREATE DATABASE tienda;

    USE tienda;

    CREATE TABLE producto(
    clave_prod int UNSIGNED ,
    nom_prod varchar(20)  PRIMARY KEY,
    precio float NOT NULL ,
    marca VARCHAR(100)
    );

    DELIMITER //
    CREATE TRIGGER trigger_check_nota_before_insert AFTER INSERT ON producto
    FOR EACH ROW BEGIN
        IF(NEW.clave_prod=NULL)
           THEN
           UPDATE producto 
           JOIN (
             SELECT nom_prod, @n := @n + 1 AS clave_prod
             FROM producto
             CROSS JOIN (SELECT @n := (SELECT MAX(clave_prod) FROM producto)) AS v
             WHERE clave_prod IS NULL
             ORDER BY clave_prod
           ) AS producto2 ON producto.nom_prod = producto2.nom_prod
           SET producto.clave_prod = producto2.clave_prod;
        END IF;
        END//
    DELIMITER ;


    INSERT INTO producto VALUES (1,'1CAFÉ KG',105,'Nestle');
    INSERT INTO producto VALUES (NULL,'2CAFÉ KG',10,'Nestle');
    INSERT INTO producto VALUES (NULL,'3CAFÉ KG',1,'Nestle');
    INSERT INTO producto VALUES (NULL,'4CAFÉ KG',1405,'Nestle');

https://www.db-fiddle.com/f/qPV662LxGenZ3HKCJCJPS5/0 - Consultas

# Ejercicios moodle

https://www.db-fiddle.com/f/4wTCZtj8UY48Lai8En1AEk/0 - 6. Creación de una Base de Datos

https://www.db-fiddle.com/f/4wTCZtj8UY48Lai8En1AEk/1 - 7. Funciones en SQL

https://www.db-fiddle.com/f/eQZ3FBhXE3knmizPH6BuGE/0 - 8. Disparadores

https://www.db-fiddle.com/f/4wTCZtj8UY48Lai8En1AEk/2 - 9. Operaciones en una base de datos

https://www.db-fiddle.com/f/rzWRTWr8qNfdijHVzkME4y/0 - Completo
