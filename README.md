# TechStore — Consultas Básicas SELECT

**Autora:** Julieta Gatica
**Fecha:** 25-09-2026

## ¿Por qué es mala práctica usar SELECT * en producción?

Usar SELECT * en producción es una mala práctica porque puede afectar el rendimiento al traer datos innecesarios. En el caso de TechStore, la tabla de sales tiene 9 columnas. Finanzas necesita 3 para sus análisis. Con SELECT * moves toda la información y ese costo se paga en cada ejecución, todos los días.
A su vez, la estructura puede contener información sensible a día de hoy, o también puede ser agregada a futuro, como el DNI del cliente, email, dirección, entre otros. Esta información no fue autorizada a que se visibilice por determinados usuarios o a que salgan de la base.


## ¿Por qué son importantes los alias para un stakeholder no técnico?

Los alias son importantes porque permiten presentar los datos con nombres claros y comprensibles para el stakeholder. 
En TechStore, el equipo de finanzas no entiende nombres técnicos en inglés. Sin alias el equipo veía order_date, product_name, quantity, estos encabezados pasaron a ser fecha_pedido, nombre_producto, cantidad_unidades. El alias es la última oportunidad de nombrar el dato antes de que salga del control del analista.# sql-select-fundamentals
