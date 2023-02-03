# LegoBD
Desenvolvimento de um modelo relacional simulando uma fabrica da LEGO


Para dar inicio na atividade fizemos um planejamento completo utilizando os modelos logico e conceitual.



MODELO LOGICO  

![328720938_569974578504834_5918595721663644858_n](https://user-images.githubusercontent.com/94478634/216650135-4757d947-15dc-47f9-b401-ca3a62b5609a.jpg)



MODELO CONCEITUAL

![329090368_725624082339162_1309501870087126676_n](https://user-images.githubusercontent.com/94478634/216650164-a483dddd-21a2-4929-a1cf-bf402cf5507d.jpg)





Então vamos criar o banco dbLego e todas as tabelas no banco e inserir os dados para dar segmento nos modelos

CREATE DATABASE BDLEGO


USE BDLEGO

CREATE TABLE COLORS(

id  int,
name varchar(500),
rgb varchar(500),
is_trans varchar(500)
)



INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(1,'Blue','0055BF','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(2,'Green','237841','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(3,'Dark Turquoise','008F9B','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(4,'Red','C91A09','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(5,'Dark Pink','C870A0','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(6,'Brown','583927','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(7,'Light Gray','9BA19D','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(8,'Dark Gray','6D6E5C','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(9,'Light Blue','B4D2E3','f');
INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(10,'Bright Green','4B9F4A','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(11,'Light Turquoise','55A5AF','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(12,'Salmon','F2705E','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES(13,'Pink','FC97AC','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES('14','Yellow','F2CD37','f');

INSERT INTO `colors`(`id`, `name`, `rgb`, `is_trans`) 
VALUES('15','White','FFFFFF','f');



CREATE TABLE  THEMES(
id int ,
name varchar(500),
parent_id int 
);



INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (1,'Technic',1);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (2,'Arctic Technic',1);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (3,'Competition',1);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (4,'Expert Builder',1);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (5,'Model',1);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (6,'Airport',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (7,'Construction',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (8,'Farm',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (9,'Fire',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (10,'Harbor',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (11,'Off-Road',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (12,'Race',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (13,'Riding Cycle',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (14,'Robot',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (15,'Traffic',5);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (16,'RoboRiders',1);
INSERT INTO `themes`(`id`, `name`, `parent_id`) 
VALUES (17,'Speed Slammers',1);





CREATE TABLE  SETS(
set_num int,
name varchar(500),
year varchar(20),
theme_id int,
num_parts int
);

INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (00-1,'Weetabix Castle','1970',414,471);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (0011-2,'Town Mini-Figures','1978',84,12);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (0011-3,'Castle 2 for 1 Bonus Offer','1987',199,2);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (0012-1,'Space Mini-Figures','1979',143,12);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (0013-1,'Space Mini-Figures','1979',143,12);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (0014-1,'Space Mini-Figures','1979',143,12);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (0015-1,'Space Mini-Figures','1979',143,18);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (0016-1,'Castle Mini Figures','1978',186,15);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (00-2,'Weetabix Promotional House 1','1976',413,147);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (00-3,'Weetabix Promotional House 2','1976',413,149);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (00-4,'Weetabix Promotional Windmill','1976',413,126);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (005-1,'Basic Building Set in Cardboard','1965',366,35);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (00-6,'Special Offer','1985',67,3);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (00-7,'Weetabix Promotional Lego Village','1976',413,3);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (010-1,'Basic Building Set in Cardboard','1965',366,57);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (010-3,'Basic Building Set','1968',366,77);
INSERT INTO `sets`(`set_num`, `name`, `year`, `theme_id`, `num_parts`) 
VALUES (011-1,'Basic Building Set','1968',366,145);




CREATE TABLE  PARTS(
part_num int,
name varchar(500),
part_cat_id int
);



INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('0687b1','Set 0687 Activity Booklet 1',17);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('0901','Baseplate 16 x 30 with Set 080 Yellow House Print',1);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('0902','Baseplate 16 x 24 with Set 080 Small White House Print',1);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('0903','Baseplate 16 x 24 with Set 080 Red House Print',1);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('0904','Baseplate 16 x 24 with Set 080 Large White House Print',1);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('1','Homemaker Bookcase 2 x 4 x 4',7);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('10','Baseplate 24 x 32',1);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('10016414','Sticker Sheet #1 for 41055-1',17);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('10019stk01','Sticker for Set 10019 - (43274/4170393)',17);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('10026stk01','Sticker for Set 10026 - (44942/4184185)',17);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('10029stk01','Sticker for Set 10029 - (4216816)',17);

INSERT INTO `parts`(`part_num`, `name`, `part_cat_id`) 
VALUES ('10036stk01','Sticker for Set 10036 - (821407)',17);






CREATE TABLE  PART_CATEGORIES(
id int,
name varchar(500)
);



INSERT INTO `part_categories`(`id`, `name`) 
VALUES (1,'Baseplates');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (2,'Bricks Printed');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (3,'Bricks Sloped');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (4,'"Duplo, Quatro and Primo"');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (5,'Bricks Special');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (6,'Bricks Wedged');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (7,'Containers');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (8,'Technic Bricks');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (9,'Plates Special');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (10,'Tiles Printed');
INSERT INTO `part_categories`(`id`, `name`) 
VALUES (11,'Bricks');



CREATE TABLE INVENTORY_PARTS(
inventory_id int,
part_num varchar(500),
color_id int,
quantity int,
is_spare varchar(20)
);




INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (1,'48379c01',72,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (1,'48395',7,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (1,'mcsport6',25,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (1,'paddle',0,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (3,'11816pr0005',78,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (3,'2343',47,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (3,'3003',29,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (3,'30176',2,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (3,'3020',15,1,'f');
INSERT INTO `inventory_parts`(`inventory_id`, `part_num`, `color_id`, `quantity`, `is_spare`)
 VALUES (3,'3022',15,2,'f');



CREATE TABLE INVENTORIES (
id int,
version varchar(500),
set_num int
);


INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (1,'1',7922-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (3,'1',3931-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (4,'1',6942-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (15,'1',5158-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (16,'1',903-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (17,'1',850950-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (19,'1',4444-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (21,'1',3474-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (22,'1',30277-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (25,'1',71012-11);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (26,'1',6435-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (27,'1',3055-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (28,'1',7899-1);
INSERT INTO `inventories`(`id`, `version`, `set_num`) 
VALUES (29,'1',1076-3);




CREATE TABLE INVENTORY_SETS (
inventory_id int ,
set_num int,
quantity int
);


INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES ( 35,75911-1,1);

INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES (35,75912-1,1);

INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES (39,75048-1,1);

INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES (39,75053-1,1);

INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES (50,4515-1,1);
INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES (50,4520-1,2);

INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES (50,4531-1,1);

INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES (71,7690-1,1);

INSERT INTO `inventory_sets`(`inventory_id`, `set_num`, `quantity`)
 VALUES (71,7691-1,1);



Então no My SQL teremos algo parecido com isso:


![image](https://user-images.githubusercontent.com/94478634/216651069-4ee7f078-d7a8-4f57-8100-cd4059fd2573.png)




agora com base no modelo vamos criar as chaves primarias e estrageiras para fazer o relacionamento funcionar corretamente


ALTER TABLE inventory_parts
ADD FOREIGN KEY (inventory_id ) REFERENCES inventories(id);


ALTER TABLE inventory_sets
ADD FOREIGN KEY (inventory_id ) REFERENCES inventories(id);



ALTER TABLE INVENTORY_PARTS
ADD FOREIGN KEY (id_parts ) REFERENCES PARTS(id );



ALTER TABLE INVENTORY_PARTS
ADD FOREIGN KEY (inventory_id ) REFERENCES  inventories(id);


ALTER TABLE parts
ADD FOREIGN KEY (part_cat_id) REFERENCES PART_CATEGORIES(id );



ALTER TABLE  criar
ADD FOREIGN KEY (num_parts_sets) REFERENCES  sets(set_num);


ALTER TABLE  criar
ADD FOREIGN KEY (id_themes) REFERENCES  THEMES(id);




vamos criar algumas consultas para dar segmento:
-------------------------------------------------




1 me de as peças da cor azul?
---------------------------------------------------------- 


SELECT *

FROM INVENTORIES

INNER JOIN COLORS C 

ON ID = ID

WHERE C.NAME = 'BLUE'

ORDER BY NAME

GROUP BY NAME


2 Qual o total de peças da cor amerala?
---------------------------------------------------------- 

SELECT COUNT(*) 

FROM INVENTORIES

INNER JOIN COLORS C 

ON ID = ID

WHERE C.NAME = 'YELLOW' 

ORDER BY NAME

GROUP BY NAME



3 Quais todos os conjuntos(sets) do ano de 1970 ? 
---------------------------------------------------------- 

SELECT * 

FROM INVETORY_SETS

INNER JOIN SETS ON  

IVENTORY_ID = SET_NUM

WHERE YEAR = '1970'


4  Quais todos os conjuntos(sets) depois de 1999 ?
---------------------------------------------------------- 

SELECT * 

FROM INVETORY_SETS

INNER JOIN SETS ON

IVENTORY_ID = SET_NUM

WHERE YEAR < '1999'



5 Quais o total de peças do invetário ?
---------------------------------------------------------- 

SELECT COUNT(*) AS total_de_peças 

FROM INVENTORIES

ORDER BY id

GROUP BY id




























