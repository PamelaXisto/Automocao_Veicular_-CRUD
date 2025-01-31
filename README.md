# 🚗 Sistema de Cadastro de Veículos 🚗

Este projeto foi desenvolvido como parte de um **estudo de caso** na **faculdade UNIFECAF** sobre **Java Programação Orientada a Objetos (POO)** com operações **CRUD**. O objetivo do sistema é possibilitar o cadastro, atualização, remoção e consulta de veículos, com funcionalidades adicionais como **filtros de busca** por características como **modelo**, **preço**, **tipo de veículo** e **ano de fabricação**. Além disso, veículos com o status **"Vendido"** são automaticamente removidos do catálogo.

---

## 🛠️ Tecnologias Usadas

- **Java 8+**: Linguagem de programação principal do projeto.
- **Spring Boot**: Framework utilizado para facilitar o desenvolvimento do back-end.
- **Spring Data JPA**: Para persistência de dados no banco de dados.
- **MySQL**: Banco de dados relacional utilizado para armazenar as informações dos veículos.
- **Maven**: Gerenciador de dependências.
- **Thymeleaf**: Template engine para o front-end (se aplicável).

---

## 💡 Funcionalidades

- **Cadastro de veículos**: Incluindo informações como **modelo**, **marca**, **ano**, **quilometragem**, **combustível**, **URL**, **status de disponibilidade**, **preço**.
- **Consulta e filtro de veículos**: Permite buscar e filtrar veículos por **marca**.
- **Exclusão automática**: Veículos com status **"Vendido"** são automaticamente removidos do catálogo.
- **Atualização e remoção de veículos**: Atualização de informações e remoção de veículos do banco de dados.

---

## 📋 Requisitos para Execução

- **Java 8 ou superior**: Necessário para rodar a aplicação.
- **MySQL**: Banco de dados configurado com a tabela **tbl_veiculos**.
- **Maven**: Para gerenciar dependências e executar o projeto.
- **IDE**: Recomenda-se utilizar o **IntelliJ IDEA** para melhor compatibilidade com o projeto.

---

## 🗂️ Estrutura do Projeto (Back-End)

A estrutura do projeto é organizada da seguinte maneira:

```plaintext
Sistema-Automotivo/
 ├── .idea/                  # Configurações do IntelliJ IDEA
 ├── src/
 │    ├── main/
 │    │    ├── java/
 │    │    │    ├── br/
 │    │    │    │    ├── com/
 │    │    │    │    │    └── fecaf/
 │    │    │    │    │        ├── controller/           # Controladores da aplicação
 │    │    │    │    │        │    └── VeiculoController.java
 │    │    │    │    │        ├── database/             # Configurações de banco de dados
 │    │    │    │    │        ├── model/                # Modelos de dados
 │    │    │    │    │        │    └── Veiculo.java
 │    │    │    │    │        ├── repository/           # Repositórios para acesso ao banco de dados
 │    │    │    │    │        │    └── VeiculoRepository.java
 │    │    │    │    │        ├── services/             # Serviços que implementam a lógica de negócios
 │    │    │    │    │        │    └── VeiculoService.java
 │    │    │    │    │        └── App.java              # Classe principal que inicia o aplicativo
 │    │    ├── resources/
 │    │    │    └── application.properties               # Arquivo de configuração do banco de dados e outras propriedades
 │    ├── test/                   # Testes da aplicação
 │    └── target/                 # Diretório gerado durante a construção do projeto
 ├── .gitignore                  # Arquivos e pastas ignorados pelo Git
 ├── pom.xml                     # Arquivo de configuração do Maven
```

## 🗂️ Estrutura do Projeto (Front-End)

```plaintext
FRONT-SISTEMA-AUTOMOTIVO/                
 ├── css/
 │    ├── styles.css/
 ├── js/
 │    ├── script.js/
 ├── index.html/
```

## 📊 Estrutura Do Banco de Dados
```bash
CREATE TABLE tbl_veiculos (
	id INT AUTO_INCREMENT PRIMARY KEY,
    modelo VARCHAR(200) NOT NULL,
    ano INT NOT NULL,
    marca VARCHAR(200) NOT NULL,
    quilometragem DECIMAL(5, 3),
    combustivel VARCHAR(100),
    disponibilidade VARCHAR(50),
    preco FLOAT(53) NOT NULL,
    foto VARCHAR(200) NOT NULL
);
```

## ⚙️ Como Rodar o Projeto Localmente

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/usuario/nome-do-repositorio.git
