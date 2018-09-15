# sql
create table custmer (cid int,cname varchar(60),mobileno bigint);
create table product (pid int,pname varchar(20),manifacture datetime);


insert into custmer values (1,'naga',9014276726);
insert into custmer values (2,'dinesh',9618744191);
insert into custmer values (4,'seshapani',9014276726);
insert into custmer values (5,'sathyamma',998918744191);


insert into product values (1,'nice','2018/03/22');
insert into product values (2,'flexone','2017/04/02');
insert into product values (3,'paracitmal','2017/12/04');


select * from product;
select * from custmer;



alter table product alter column manifacture varchar(20)

select product.pid , product.pname ,   custmer.cid,custmer.cname  from custmer, product   where  product.pid = custmer.cid;

select * from custmer inner join product on custmer.cid=product.pid;

select * from custmer left join product on custmer.cid=product.pid;

select * from custmer right join product on custmer.cid=product.pid;

select * from custmer full join product on custmer.cid=product.pid;

SELECT custmer.cname,custmer.mobileno,custmer.cid,
product.pid,   product.pname,product.manifacture 
FROM custmer 
CROSS JOIN product;


select * from custmer cross join product;
