CREATE DATABASE postogasolina;
use postogasolina;

CREATE TABLE combustiveis (
    id_combustivel INT AUTO_INCREMENT PRIMARY KEY,
    tipo VARCHAR(50) NOT NULL,
    preco_por_litro DECIMAL(5,2)
);

CREATE TABLE bombas (
id_bomba INT AUTO_INCREMENT PRIMARY KEY,
id_combustivel INT,
descricao VARCHAR(100)
);

CREATE TABLE funcionarios (
id_funcionario INT AUTO_INCREMENT PRIMARY KEY,
nome VARCHAR(100),
cargo VARCHAR(50),
turno ENUM ("m", "V", "N"),
telefone VARCHAR(15)
);

CREATE TABLE abastecimentos (
id_abastecimento INT AUTO_INCREMENT PRIMARY KEY,
id_cliente INT,
id_bomba INT,
id_funcionario INT,
volume DECIMAL(6,2),
valor_total DECIMAL(8,2),
data_abastecimento DATETIME
);

CREATE TABLE servicos (
id_servico INT AUTO_INCREMENT PRIMARY KEY,
descricao VARCHAR(255),
preco DECIMAL(8,2)
);
