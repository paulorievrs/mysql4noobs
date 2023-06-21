# Adicionando tabela 'DICIPLINA'

Vamos criar a tabela para conter as diciplinas do curso. Lembrando que uma disciplina vai pertencer a um curso, porém um curso poderá ter mais de uma disciplina.

Digite:

```sql
CREATE TABLE DICIPLINA (
    codigodiciplina int,
    nome varchar(30),
    codigocurso int,
    PRIMARY KEY (codigocurso)

    CONSTRAINT codigocurso
        FOREIGN KEY (codigocurso)
        REFERENCES CURSO(codigocurso)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);
```


















**ON UPDATE CASCADE:** Indica um 'UPDATE em cascata', ou seja, quando atualizarmos o campo 'codigocurso' de algum registro da tabela 'CURSO', então o campo 'codigocurso' data tabela 'DICIPLINA' também será atualizado.

**ON DELETE CASCADE:** Indica um 'DELETE em cascata', ou seja, quando deletarmos algum registro da tabela 'CURSO', então todos os registros da tabela 'DICIPLINA' relacionados a este serão deletados também.

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
    FOREIGN KEY (codigocurso) REFERENCES CURSO(codigocurso)
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