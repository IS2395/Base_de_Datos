# Base de datos biblioteca

https://www.db-fiddle.com/f/umEMiHGa4VmwR7Mvpf8M6Z/0
    
# Base de datos editorial

![Imagen1](https://user-images.githubusercontent.com/111446113/201251841-07b318a1-c3ab-4974-a3c2-56629b18402a.png)


https://www.db-fiddle.com/f/2VvT9JW4mFuUHwpAJF3QzH/1  -  Estructura completa

# Base de datos tienda

https://www.db-fiddle.com/f/tfg8VkdD8MqnHksHivtg9P/1 - Con Querys

https://www.db-fiddle.com/f/tfg8VkdD8MqnHksHivtg9P/2 - Querys de group by y order by


        USE tienda;
        /*enlistar clientes*/
        /*CAMBIAR NOMBRE DE CLINETE*/
        /*UPDATE cliente 
        SET nom_clie = 'Laura Peréz'
        WHERE clave_clie = 23;
        SELECT * FROM cliente;*/
        /*promedio*/
        /*SELECT AVG (precio)
        FROM producto;*/
        /*contar*/
        /*SELECT COUNT (nom_prod)
        FROM producto;*/
        /*maximo*/
        /*SELECT MAX (precio)
        FROM producto;*/
        /*minimo*/
        /*SELECT MIN (precio)
        FROM producto;*/

        /*SELECT * 
        FROM nota;*/
        UPDATE nota
        INNER JOIN producto ON producto.clave_prod=nota.clave_prod1
        SET subtot = cant * precio;
        UPDATE nota
        SET IVA = subtot * 0.16;
        UPDATE nota
        SET total = subtot + IVA;
        /*SELECT *
        FROM nota;*/
        /*SELECT folio, clave_prod, clave_clie, cant, subtot
        FROM producto INNER JOIN nota ON nota.clave_prod1 = producto.clave_prod
        INNER JOIN cliente ON cliente.clave_clie = nota.clave_clie1;*/


        /*DROP FROM nota;*/
        /*SELECT * FROM nota;*/
        /*DELETE FROM cliente
        WHERE clave_clie = 23;*/
        /*DROP DATABASE tienda*/

        /*SELECT * FROM producto;*/

        /* precio mas alto*/
        /*SELECT marca, MAX(precio)
        FROM producto
        GROUP BY marca;*/

        /*cuantos productos */
        /*SELECT marca, COUNT(nom_prod)
        FROM producto
        GROUP BY marca;*/

        /* ordernar* ascendente ordenado por clave del cliente*/
        /*SELECT nom_clie
        FROM cliente
        ORDER BY (clave_clie) ASC;*/

        /*ordenar de forma descendente*/
        /*SELECT nom_prod, precio, marca
        FROM producto
        ORDER BY (marca) DESC;*/

        SELECT total, cant
        FROM nota
        ORDER BY (subtot) ASC;


