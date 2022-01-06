create database farmacia;
use farmacia;

create table laboratorio(
codLab integer not null primary key,
laboratorio varchar(20),
telefone varchar(20));

create table remedio(
codRemedio integer not null primary key,
nomeRemedio varchar(20),
preco Decimal (10,2),
codLab integer,
foreign key (codLab) references laboratorio (codLab));

insert into laboratorio (codLab,laboratorio,telefone) values
(1,"Roche", "7777777"),
(2,"Pfizer","6666666"),
(3,"Merk","5555555");

insert into remedio (codRemedio,nomeRemedio,preco,codLab) values
(1,"Vitamina C",13.00,1),
(2,"Azitromicina",24.90,3),
(3,"Advil",19.42,2);

select * from laboratorio;
select * from remedio;






