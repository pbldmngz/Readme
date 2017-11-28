# Readme
First SQL Conection
INSTRUCCIONES DE INICIO
	► REQUERIMIENTOS:
		- XAMPP. https://www.apachefriends.org/es/download.html
		- SQL Developer. http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html
		- JDBC Driver. http://www.oracle.com/technetwork/database/features/jdbc/index-091264.html
	► INSTALACIÓN:
		- Descargar los archivos donde sea conveniente
		- Intalar los dos primeros programas
		- Extraer JDBC Driver en algún lugar (no es relevante)
		- Abrir SQL Developer
			- Ir a herramientas> Preferencias> Base de Datos> Controladores JDBC de Terceros
			- Agregar entrada
			- Buscar la ubicación del archivo descomprimido (JDBC Driver), listo
			- Aceptar
		- Abrir XAMPP (XAMPP Control Panel)
			- Iniciar Apache y MySQL
			- No cerrarlo hasta terminar de trabajar
		- Agregar una nueva conexión en SQL Developer mediante la cruz verde en el apartado de conexiones (arriba a la izquierda, debajo de la barra de navegación)
			Todo lo que no se mencione no se cambia:
			- Nombre de la conexión: localhost@test_database
			- Usuario: root
			- Pestaña MySQL
				- Nombre del host: localhost
				- Puerto: 3306
				- Selecciona tu base de datos
			- Conectar
	► DESARROLLO
		- Abrir el navegador
		- Buscar "localhost" en la barra de direcciones
		- Abrir la pestaña phpMyAdmin
		- En la pestaña de bases de datos de la izquierda, crear una nueva llamándola "dwdb_test"
		- Crea una nueva tabla con el nombre "products"
			- Categoría con el nombre "product_id"
			- Categoría con el nombre "product_name" y establecer que se trata de un tipo varchar con extensión de 100
			- Categoría con el nombre "product_price"
			- Categoría con el nombre "product_category_id"
		- Abrir el SQL Developer
		- Ir a tu base de datos y añadir *este* código dentro de la hoja de trabajo de SQL
*este*
      -- INSERTAR CATEGORÍAS DE PRODUCTOS --
insert into product_category values(1, 'Comida');
insert into product_category values(2, 'Cena');
insert into product_category values(3, 'Desayuno');
insert into product_category values(4, 'Postre');
insert into product_category values(5, 'Bebidas');
insert into product_category values(6, 'Snacks');
insert into product_category values(7, 'Merienda');

select *
from product_category;

--Esto sirve para hslalahslahslah FT. KANTER
    -- Esta es una herramienta mágica que nos servirá más tarde...:.::::::::.
--delete from products where product_id in (1,2,3,4,5,6,7);

-- INSERTAR PRODUCTOS DENTRO DE CATEGORÍAS --
INSERT into products VALUES (36, 'Pulpo a la gallega', 170, 1);  
INSERT into products VALUES (37, 'Tortilla española', 120, 1);
INSERT into products VALUES (38, 'Paleta de cordero', 270, 1);
INSERT into products VALUES (39, 'Cabrito', 2000, 1);
INSERT into products VALUES (40, 'Chuletón de res', 270, 1);

INSERT into products VALUES (6, 'Ensalada de pollo', 70, 2);
INSERT into products VALUES (7, 'Alitas de pollo', 100, 2);
INSERT into products VALUES (8, 'Tacos', 40, 2);
INSERT into products VALUES (9, 'Lágrimas de pollo', 170, 2);
INSERT into products VALUES (10, 'Carnes frías', 170, 2);

INSERT into products VALUES (11, 'Chilaquiles', 170, 3);
INSERT into products VALUES (12, 'Torta', 120, 3);
INSERT into products VALUES (13, 'Club sandwich', 170, 3);
INSERT into products VALUES (14, 'Huevos revueltos', 370, 3);
INSERT into products VALUES (15, 'Ensalada murciana', 70, 3);

INSERT into products VALUES (16, 'Leche frita', 50, 4);
INSERT into products VALUES (17, 'Nieve de temporada', 40, 4);
INSERT into products VALUES (18, 'Tarta santiago', 30, 4);
INSERT into products VALUES (19, 'Flan granadino', 60, 4);
INSERT into products VALUES (20, 'Volcán de chocolate', 700, 4);

INSERT into products VALUES (21, 'Refresco', 20, 5);
INSERT into products VALUES (22, 'Vino', 70, 5);
INSERT into products VALUES (23, 'Cerveza', 40, 5);
INSERT into products VALUES (24, 'Agua', 20, 5);
INSERT into products VALUES (25, 'Jugo', 20, 5);

INSERT into products VALUES (26, 'Lágrimas de pollo', 100, 6);
INSERT into products VALUES (27, 'Patatas brazas', 60, 6);
INSERT into products VALUES (28, 'Lomo enchorizado', 60, 6);
INSERT into products VALUES (29, 'Tabla de quesos', 170, 6);
INSERT into products VALUES (30, 'Alitas de pollo', 100, 6);

INSERT into products VALUES (31, 'Serranito', 85, 7);
INSERT into products VALUES (32, 'Pizza española', 140, 7);
INSERT into products VALUES (33, 'Flan de chocolate', 110, 7);
INSERT into products VALUES (34, 'Torta de jamón serrano', 85, 7);
INSERT into products VALUES (35, 'Sándwich', 75, 7);

--FFFFFFFFFFFFFFFFFIIIIIIIIIIIIIIIIIIIIIIIIIIIINNNNNNNNNNNNNNNNNNNNNNNNNNN--

select *
from sales; 
    -- VENTA 1 --
INSERT into sales VALUES (55, 36, 1);
INSERT into sales VALUES (55, 6, 2);
INSERT into sales VALUES (55, 11, 3);
INSERT into sales VALUES (55, 16, 4);
    -- VENTA 2 --
INSERT into sales VALUES (89, 21, 5);
INSERT into sales VALUES (89, 26, 6);
INSERT into sales VALUES (89, 31, 7);
INSERT into sales VALUES (89, 37, 1);
    -- VENTA 3 --
INSERT into sales VALUES (144, 7, 2);
INSERT into sales VALUES (144, 12, 3);
INSERT into sales VALUES (144, 17, 4);
INSERT into sales VALUES (144, 22, 5);
    -- VENTA 4 --
INSERT into sales VALUES (233, 27, 6);
INSERT into sales VALUES (233, 32, 7);
INSERT into sales VALUES (233, 38, 1);
INSERT into sales VALUES (233, 8, 2);
    -- VENTA 5 --
INSERT into sales VALUES (377, 13, 3);
INSERT into sales VALUES (377, 18, 4);
INSERT into sales VALUES (377, 23, 5);
INSERT into sales VALUES (377, 28, 6);
    -- VENTA 6 --
INSERT into sales VALUES (610, 33, 7);
INSERT into sales VALUES (610, 39, 1);
INSERT into sales VALUES (610, 9, 2);
INSERT into sales VALUES (610, 14, 3);
    -- VENTA 7 --
INSERT into sales VALUES (987, 19, 4);
INSERT into sales VALUES (987, 24, 5);
INSERT into sales VALUES (987, 29, 6);
INSERT into sales VALUES (987, 34, 7);
    -- VENTA 8 --
INSERT into sales VALUES (1597, 40, 1);
INSERT into sales VALUES (1597, 10, 2);
INSERT into sales VALUES (1597, 15, 3);
INSERT into sales VALUES (1597, 20, 4);
    -- VENTA 9 --
INSERT into sales VALUES (2584, 25, 5);
INSERT into sales VALUES (2584, 30, 6);
INSERT into sales VALUES (2584, 35, 7);
INSERT into sales VALUES (2584, 36, 1);
    -- VENTA 10 --
INSERT into sales VALUES (4181, 6, 2);
INSERT into sales VALUES (4181, 11, 3);
INSERT into sales VALUES (4181, 16, 4);
INSERT into sales VALUES (4181, 21, 5);
    -- VENTA 11 --
INSERT into sales VALUES (6765, 26, 6);
INSERT into sales VALUES (6765, 31, 7);
INSERT into sales VALUES (6765, 37, 1);
INSERT into sales VALUES (6765, 7, 2);
    -- VENTA 12 --
INSERT into sales VALUES (10946, 12, 3);
INSERT into sales VALUES (10946, 17, 4);
INSERT into sales VALUES (10946, 22, 5);
INSERT into sales VALUES (10946, 27, 6);
    -- VENTA 13 --
INSERT into sales VALUES (17711, 32, 7);
INSERT into sales VALUES (17711, 38, 1);
INSERT into sales VALUES (17711, 8, 2);
INSERT into sales VALUES (17711, 13, 3);
    -- VENTA 14 --
INSERT into sales VALUES (28657, 18, 4);
INSERT into sales VALUES (28657, 23, 5);
INSERT into sales VALUES (28657, 28, 6);
INSERT into sales VALUES (28657, 33, 7);
    -- VENTA 15 --
INSERT into sales VALUES (46368, 39, 1);
INSERT into sales VALUES (46368, 9, 2);
INSERT into sales VALUES (46368, 14, 3);
INSERT into sales VALUES (46368, 19, 4);
    -- VENTA 16 --
INSERT into sales VALUES (75025, 24, 5);
INSERT into sales VALUES (75025, 29, 6);
INSERT into sales VALUES (75025, 34, 7);
INSERT into sales VALUES (75025, 40, 1);
    -- VENTA 17 --
INSERT into sales VALUES (121393, 10, 2);
INSERT into sales VALUES (121393, 15, 3);
INSERT into sales VALUES (121393, 20, 4);
INSERT into sales VALUES (121393, 25, 5);
    -- VENTA 18 --
INSERT into sales VALUES (196418, 30, 6);
INSERT into sales VALUES (196418, 35, 7);
INSERT into sales VALUES (196418, 36, 1);
INSERT into sales VALUES (196418, 6, 2);
    -- VENTA 19 --
INSERT into sales VALUES (317811, 10, 3);
INSERT into sales VALUES (317811, 16, 4);
INSERT into sales VALUES (317811, 21, 5);
INSERT into sales VALUES (317811, 26, 6);
    -- VENTA 20 --
INSERT into sales VALUES (514229, 31, 7);
INSERT into sales VALUES (514229, 37, 1);
INSERT into sales VALUES (514229, 7, 2);
INSERT into sales VALUES (514229, 11, 3);

-- Código por ejecutar ft. Kanter
select *
from sales s1
join products p1
  on s1.product_id = p1.product_id
join product_category pc1
  on pc1.product_category_id = s1.product_category_id;

select s1.sale_id,
p1.product_name, 
p1.product_price,
pc1.category_name
from sales s1
join products p1
  on s1.product_id = p1.product_id
join product_category pc1
  on pc1.product_category_id = s1.product_category_id;

select s1.sale_id,
p1.product_name, 
p1.product_price,
pc1.category_name
from sales s1
join products p1
  on s1.product_id = p1.product_id
join product_category pc1
  on pc1.product_category_id = s1.product_category_id
group by s1.sale_id;

select s1.sale_id,
p1.product_name, 
p1.product_price,
pc1.category_name
from sales s1
join products p1
  on s1.product_id = p1.product_id
join product_category pc1
  on pc1.product_category_id = s1.product_category_id
where s1.sale_id in (1, 3, 5, 7, 9, 11, 13,15)
group by s1.sale_id;
