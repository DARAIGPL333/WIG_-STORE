*/I Created a  wig store that is specialized in selling a wide variety of wigs focus on providing high-quality wigs, The store's inventory includes synthetic wigs, human hair wigs, lace front wigs, cosplay wigs, and more*/


CREATE TABLE WIGS_STORE(id INTEGER PRIMARY KEY
,item TEXT,Material_w TEXT,
lenght_lace TEXT ,Quantity INTEGER, 
hair_lenght INTEGER,price INTEGER);

INSERT INTO wigs_store VALUES( 1,"BLOND WIG","HUMAN",2,40,5000);
INSERT INTO wigs_store VALUES(2," bob wig","synthetic","middle part" ,5,10,800);
INSERT INTO wigs_store VALUES( 3,"pink wig","blended" ,4x4,1,20,1500);
INSERT INTO  wigs_store VALUES(4,"highlight wig","human",13x6 ,3,30,2500);
INSERT INTO wigs_store VALUES(5,"ginger wig","human","middle part", 4,35,4000);
INSERT INTO wigs_store VALUES( 6,"black curly wig","human",13x6,4,40,6000);
INSERT INTO wigs_store VALUES(7,"platinum wig","blended",4x4, ,3,30,5000);
INSERT INTO wigs_store VALUES( 8,"locs wig","blended", "middle part",6,40,1000);
INSERT INTO wigs_store VALUES(9,"rainbow wig","synthetic",4x4,7,35,500);
INSERT INTO wigs_store VALUES(10,"red wig","human",4x4,9,22,1200);
INSERT INTO wigs_store VALUES(11,"yellow wig","human",13x6,2,26,3000);
INSERT INTO wigs_store VALUES(12,"grenn bob wig","human"," middle part",4,12,700);
INSERT INTO wigs_store VALUES(13,"orange wig","human","middle part",4,30,2000);
INSERT INTO wigs_store VALUES(14,"light brown wig","human",13x6, 4,35,4500);
INSERT INTO wigs_store VALUES(15," blue wig","human",13x6,4,30,3500);


select
*
FROM wigs_store

*/ the Wig Store provides customers with a wide range of options, from affordable synthetic wigs to premium human hair wigs
 top 5 most expensive wigs:*/

SELECT *
FROM wigs_store 
ORDER BY Price DESC
LIMIT 5 ;


*/ Get the average price for all wigs in the wigs_store table where the material is 'human'. */

SELECT
id
AVG(Price) AS AveragePrice 
FROM wigs_store
WHERE material_w ='human" desc;


*/ Getting  the total value of each wig  type in stock*/

SELECT 
material_w
SUM(price * Quantity) AS TotalValue 
FROM wigs_store
GROUP BY material_w;









