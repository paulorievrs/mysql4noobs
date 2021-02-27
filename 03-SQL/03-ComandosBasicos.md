# Comandos Básicos
Existem alguns comandos básicos para utilizar um banco de dados SQL, como por exemplo para buscar dados, altera-los, deleta-los e inseri-los.

# Criação de um banco

```sql
CREATE DATABASE BANCODEDADOS;
```

Cria um banco de dados denominado BANCODEDADOS.

# Criação de uma tabela

```sql
CREATE TABLE TABELA (
    ID int,
    CAMPO1 varchar(255),
    CAMPO2 varchar(255)
);
``` 
Cria uma tabela chamada TABELA, com o campo ID como inteiro, CAMPO1 como varchar(255) e CAMPO2 como varchar(255).

Os valores 255 são o tamanho de caracteres que o campo pode ter.

# Inserir

Para inserirmos dados utilizamos o comando:
```sql
INSERT INTO TABELA (CAMPO1, CAMPO2) VALUES (VALOR1, VALOR2)
```
Esse comando insere na tabela TABELA, nos campos CAMPO1 e CAMPO2 os valores respectivamente na ordem VALOR1 e VALOR2

# Buscar

Para buscarmos dados utilizamos o comando:

```sql
SELECT * FROM TABELA
```

Esse comando busca todos os dados de todas as colunas da tabela TABELA.

Podemos filtrar melhor com: 
```sql
SELECT CAMPO1, CAMPO2 FROM TABELA
```

Assim buscando somente os campos CAMPO1 e CAMPO2 do banco e não todos eles.

# Alterar

Para alterarmos dados utilizamos o comando:

```sql
UPDATE TABELA SET CAMPO1 = 'VALOR ALTERADO';
```

Temos que tomar cuidado com esse tipo de comando pois com isso alteraremos todos os dados da tabela TABELA colocando o valor do CAMPO1 como VALOR ALTERADO. Mais abaixo ensinarei como previnir isso.

# Deletar

Para deletarmos dados utilizamos o comando:

```sql
DELETE FROM TABELA;
```
Temos que tomar cuidado pois esse comando irá deletar todos os dados da tabela TABELA.

# WHERE

O WHERE é um comando muito utilizado e por para realizar alterações de deleções em tabelas é extremamente necessário.

Para alterarmos um campo específico podemos utilizar o comando:


```sql
UPDATE TABELA SET CAMPO1 = 'VALOR ALTERADO' WHERE ID = 1;
```

Nesse caso estamos dizendo para o SQL para alterar o CAMPO1 da tabela TABELA somente aonde o campo ID seja igual a 1, e geralmente os campos de ID tem valor únicos, são PRIMARY KEYS, por isso é necessário realizar essa operação de alteração utilizando o comando WHERE.

Para deletarmos um campo específico podemos utilizar o comando:

```sql
DELETE FROM TABELA WHERE ID = 1;
```

Agora estamos deletando um campo da tabela TABELA somente aonde o seu ID é 1, para assim conseguirmos ter melhor filtragem e não deletar dados que não deveriam.

Além de deletar e alterar, o comando WHERE pode ser utilizado para buscas de dados também, trazendo assim maior filtragem: 

```sql
SELECT * FROM TABELA WHERE ID = 1;
```

Assim, busca somente os dados da tabela TABELA aonde o ID for igual a 1. 

# AND / OR

É possível utilizar expressões lógicas para realizar operações de banco, como no exemplo:

```sql
SELECT * FROM TABELA WHERE ID = 1 OR ID = 2;
```

Nesse caso trazemos dados aonde o ID seja igual a 1 OU igual 2.

```sql
SELECT * FROM TABELA WHERE CAMPO1 = 'MYSQL' AND CAMPO2 = '4NOOBS';
```

Nesse caso só trazemos dados aonde o CAMPO1 do seja igual a MYSQL e o CAMPO2 seja igual a 4NOOBS.

# LIKE

Podemos aprimorar mais ainda o WHERE, colocando o valor de LIKE nele, aonde é buscado um valor "parecido" com um passado.

```sql
SELECT * FROM TABELA WHERE CAMPO1 LIKE '%MYSQL%';
```
As '%' dizem aonde irá ser feita a busca, se colocar antes e depois da palavra quer dizer que vai buscar strings que tenham o valor MYSQL em qualquer lugar. Se colocar assim: 

```sql
SELECT * FROM TABELA WHERE CAMPO1 LIKE '%MYSQL';
```

Irá buscar somente dados que tem a palavra MYSQL no final e assim:

```sql
SELECT * FROM TABELA WHERE CAMPO1 LIKE 'MYSQL%';
```

Irá buscar somente dados que tem a palavra MYSQL no início.

#

Eu sei que foi bastante coisaa até agora, mas quando o conteúdo começar a ser aplicado na prática irá ficar mais simples e fácil.

<a href="../04-Projeto/01-IniciandoProjeto.md">Próximo -></a>