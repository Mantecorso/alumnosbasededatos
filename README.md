# alumnosbasededatos



    1.Crea una base de datos denominada vuelos. Con las siguientes características:

    Character set = Latin1
    Collate = latin1_spanish_ci


CREATE DATABASE vuelos CHARACTER SET Latin1;

ALTER DATABASE vuelos COLLATE latin1_spanish_ci;


    2.Renombra la base de datos a viajes.

TODAVIA NO SABEMOS, hay que volcar los datos a un archivo bmp y luego creaer nueva base de datos con el nombre nuevo e importar los datos.


    3.Crea una tabla denominada clientes que contendrá los siguientes campos:

    id
        Integer
        autoincremental
        not_null
        primary_key
    nombre
        varchar(50)
    apellidos
        varchar(50)
    direccion
        varchar(150)



USE vuelos;

CREATE TABLE clientes(
	id integer auto_increment primary key,
    nombre varchar(50),
    apellidos varchar(50),
    direccion varchar(150)
);


    4.Crea una tabla denominada viajes que contendrá los siguientes campos:

    id
        Integer
        autoincremental
        not_null
        primary_key

    titulo
        varchar(50)

    descripcion
        varchar(150)

    codigoCliente *Integer *Forgein key clientes(id)


USE vuelos;

    CREATE TABLE viajes(
	id integer auto_increment primary key,
    titulo varchar(50),
    descripcion varchar(150),
    codigoCliente integer, 
    FOREIGN KEY (codigoCliente) REFERENCES clientes(id)
);
