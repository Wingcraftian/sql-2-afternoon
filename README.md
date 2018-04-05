/* Everything deleted from practice updating rows and up by mistake*/
/* Update customer set company = "Self" where company is Null; */
/* Select company from customer */
/* update customer set LastName = "Thompson" where FirstName = "Julia" and LastName = "Barnett" */
/* Select firstName, lastName from customer */
/* update customer 
set supportrepid = 4
where email = "luisrojas@yahoo.cl"; */
/* Update track 
set composer = "The darkness around us" where genreid = 3 and composer is null; */
/* ^^^^Manuel method^^^^ */
/* Select * from genre; */
/* update track
set composer ="The darkness around us"
where genreid = ( select genreid from genre where name = "Metal") 
and composer is null; */

/* SELECT count(*), g.name
from track t
join genre g ON t.genreid = g.genreId
group by g.name; */


/* SELECT count(*),g.name
from track t
join genre g ON t.genreid = g.genreid
where g.name = "Pop" or g.name = "Rock"
group by g.name; */

/* SELECT count(*), art.name
from album alb
join artist art ON alb.artistid=art.artistid
group by art.artistid */


/* Use distinct */

/* SELECT DISTINCT composer
from track; */

/* SELECT DISTINCT billingpostalcode
from invoice; */

/* SELECT Distinct company
from customer; */
/*  Delete Rows */

/* Delete from practice_delete where type = "bronze"; */
/* Delete from practice_delete where type = "silver"; */
/* Delete from practice_delete where value = 150; */
/* SELECT * FROM practice_delete; */


/* create table users (
userid integer primary key autoincrement,
name varchar(512),
  email varchar(512)
); */
/* select * from users; */
/* create table products (
  productid integer primary key autoincrement,
  name varchar(512),
  price float(2)
); */

/* create table orders (
  id integer primary key autoincrement,
Quantity integer,
productid integer,
  userid integer,
  FOREIGN KEY(productid) REFERENCES products(productid),
  FOREIGN KEY(userid) REFERENCES users(userid)
  ); */
/* Drop table orders; */
/* drop table users; */

/* drop table products; */

/* insert into products ( name, price)
values
("Razer", 123),
("apple", 999999),
("Backpack", 80);  */
/* select * from products; */

/* insert into users 
(name,email)
values
("Jacob","Jacob.fakeemail@gmail.com"),
("Levi","FakeEmail@Yahoo.com"),
("Jerry","JerryatAnotherfakeemail@mac.com"); */

/* Updated table */

/* insert into orders
(quantity,productid,userid)
values 
(10,1,1), 
(1,2,3), 
(1,3,2); */

/* select * from products */
/* select * from orders; */
/* select name 
from products 
where productid In(Select productId from orders Where id = 1); */
/* Select * from orders; */
/* one above was for get all orders, I couldn't tell if it meant something special about that */

/* Select sum(o.quantity*p.price)
from orders o
join products p On p.productid = o.productid
where o.productid = 1; */


/*  Select p.name, u.name, o.quantity
from orders o
join products p on o.productid = p.productid
join users u on o.userid = u.userid 
where u.name = 'Jacob';
 */
/* Select count(o.id), u.name 
from users u
join orders o on o.userid = u.userid 
group by o.userid; */
/* Inserting an extra order to see if working properly */
/*  insert into orders
(quantity,productid,userid)
values 
(10,2,1); */


