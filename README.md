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

# BIBLIOTECA

CREATE DATABASE biblioteca;
USE biblioteca;

CREATE TABLE livro
(
id_l INT AUTO_INCREMENT PRIMARY KEY,
livro_id VARCHAR(100)
);


CREATE TABLE autor
(
id_a INT AUTO_INCREMENT PRIMARY KEY,
autor_id VARCHAR(100)
);

INSERT INTO livro (livro_id) VALUES
('Assasinato no expresso oriente'),
('Harry potter e a pedra filosofal'),
('Senhor dos aneis');

INSERT INTO autor (autor_id) VALUES
('Agatha Christie'),
('J.K.Rolling'),
('Tolkien');

CREATE TABLE biblioteca
(
id INT AUTO_INCREMENT PRIMARY KEY,
autor_id INT,
livro_id INT,
data_m DATE,
FOREIGN KEY (autor_id) REFERENCES autor(autor_id),
FOREIGN KEY (livro_id) REFERENCES livro(livro_id)
);

INSERT INTO biblioteca (autor_id, livro_id) VALUES
('1', '1'),
('2', '2');


); 
INSERT INTO lucro(receita, despesa, lucro, data_dia) VALUES 
('1000000.00', '25000.00', '750000.00' , '2012-01-06') ;

SELECT * FROM  lucro;

# COISA QUE EU COPIEI

CREATE DATABASE escola;
USE escola;


CREATE TABLE pessoa 
(
id_pessoa INT AUTO_INCREMENT PRIMARY KEY,
nome VARCHAR(100)
);

CREATE TABLE professor 
(
id_professor INT AUTO_INCREMENT PRIMARY KEY,
id_pessoa INT,
FOREIGN KEY (id_pessoa) REFERENCES pessoa(id_pessoa)
);

CREATE TABLE aluno 
(
id_aluno INT AUTO_INCREMENT PRIMARY KEY,
id_pessoa INT,
FOREIGN KEY (id_pessoa) REFERENCES pessoa(id_pessoa)
);

INSERT INTO pessoa (nome) VALUES
('pedro lopes'),
('paulo');

INSERT INTO aluno (id_pessoa) VALUES
(NULL),
(2);
INSERT INTO professor (id_pessoa) VALUES
(1),
(NULL);

SELECT 
    p.id_pessoa,
    p.nome,
    CASE
        WHEN pr.id_pessoa IS NOT NULL THEN 'Professor'
        WHEN al.id_pessoa IS NOT NULL THEN 'aluno'
        ELSE 'Neither'
    END AS role
FROM 
    pessoa p
LEFT JOIN 
    professor pr ON p.id_pessoa = pr.id_pessoa
LEFT JOIN 
    aluno al ON p.id_pessoa = al.id_pessoa;
