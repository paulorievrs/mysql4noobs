# Iniciando projeto

Em primeiro lugar, vamos construir uma base de dados dentro do nosso banco. Abra seu local para executar query's. No windows seria o MySQL Workbench e no Linux o proprio terminal. A sintaxe é a mesma para ambos, é só seguir o que foi apresentando na <a href="../01-Ambiente">configuração do ambiente</a> para iniciarmos.

Digite:

```sql
CREATE DATABASE FACULDADE;
```
Com isso, criamos nossa base de dados denominada FACULDADE.

Agora devemos dizer ao SQL que vamos utilizar o banco de dados FACULDADE com o comando:

```sql
USE FACULDADE;
```

Agora podemos criar suas duas tabelas, de ALUNO e CURSO, na ordem abaixo:

## Curso

```sql
CREATE TABLE CURSO (
    codigocurso int,
    nomecurso varchar(100),
    PRIMARY KEY (codigocurso)
);
```
Criamos um curso com seu código curso de valor inteiro, o definindo como primary key. Além disso, definimos que o nome do curso é um VARCHAR de valor máximo 100 caracteres.

## Aluno

```sql
CREATE TABLE ALUNO (
    matricula int,
    nome varchar(100),
    telefone varchar(11),
    codigocurso int NOT NULL,
    PRIMARY KEY (matricula),
    FOREIGN KEY (codigocurso) REFERENCES CURSOS(codigocurso)
);
```

Criamos um aluno, que tem seu número de matrícula com um valor inteiro, seu nome como um valor de VARCHAR limitado a 100 caracteres, um telefone com valor VARCHAR de 11 caracteres e definimos um valor inteiro de codigocurso para armazenarmos o código do curso que o aluno faz parte, e dizemos também que ele não pode ser nulo com a constraint NOT NULL. Além disso, devemos dizer ao SQL que o codigocurso é uma chave estrageira (foreign key) que referencia a tabela cursos no campo codigocurso, coincidentemente com o mesmo nome.

Com isso, você pode verificar as tabelas existentes no seu banco com o comando:

```sql
SHOW TABLES;
```
E se quiser ver o que compõe essa tabela é só utilizar:

```sql
DESCRIBE ALUNO;
```
Nesse caso utilizando a tabela aluno como exemplo.


<a href="./02-InserindoValores.md">Próximo -></a>