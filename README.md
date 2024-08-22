# Bancode-dados

 # Exercicio 2
 
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

