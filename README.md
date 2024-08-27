# Bancode-dados

 # CLIENTE
 
CREATE DATABASE cliente; 
USE cliente;  
CREATE TABLE cliente( 
id INT AUTO_INCREMENT PRIMARY KEY, 
nome VARCHAR(100) NOT NULL, 
cpf VARCHAR(100), 
endereço VARCHAR(100),  
data_dia DATE

); 
INSERT INTO cliente (nome, cpf, endereço, data_dia) VALUES 
('Pedro', '14081438951', 'Jardim das americas rua brigadeiro martim 1234' , '2012-01-06') ;

SELECT * FROM  cliente;
# LUCRO
CREATE DATABASE lucro; 
USE lucro;  
CREATE TABLE lucro( 
id INT AUTO_INCREMENT PRIMARY KEY, 
receita DECIMAL (10,2) NOT NULL, 
despesa DECIMAL (10,2) NOT NULL, 
lucro   DECIMAL (10,2) NOT NULL,  
data_dia DATE

); 
INSERT INTO lucro(receita, despesa, lucro, data_dia) VALUES 
('1000000.00', '25000.00', '750000.00' , '2012-01-06') ;

SELECT * FROM  lucro;


