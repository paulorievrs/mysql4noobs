# Comandos básicos do MYSQL no terminal

Além do MYSQL poder ser acessado por programas como o Workbench, Datagrip, DBeaver e outros ele também pode ser acessado e manipulado pelo terminal o que é útil para trabalhar quando é necessário acessar o Banco por SSH em algum servidor ou até mesmo para manipulação por esse meio quando necessário que isso seja feito de forma simples e rápido.

> Caso esteja usando Windows é recomendável usar o **cmder** que emula um ambiente UNIX, caso esteja usando MAC ou Linux basta usar o terminal padrão de seu Sistema Operacional / Distribuição.

## Conectar ao MYSQL

O primeiro passo é conectar ao MYSQL que está rodando em sua máquina, isso é bastante simples e pode ser feito com o comando:
```
$ mysql -u <usuário> -p
```
Exemplo: Caso queira acessar com o usuário ROOT basta:
```
$ mysql -u root -p
```
E então entrar com a senha do usuário.

O comando tem os seguintes parâmetros:
- **-u** (que também pode ser usado como **--user**): Serve para indicar o nome do usuário que será usado para se conectar.
- **-p** (que também pode ser usado como **--password**): É a senha usada para se conectar ao servidor. Se usado na forma reduzida **-p** o MySQL vai mostrar um prompt perguntando qual a senha do usuário.

> Caso o usuário que você configurou na instalação não possua senha, você pode omitir o parâmetro **-p**, porém não é recomendado que você tenha usuários sem senha por motivos de segurança do seu banco.

## Listar os Banco de Dados

Com o prompt ativo, agora podemos listar as databases que temos em nossa instância do MySQL, para isso use o comando:
```
mysql> show databases;
``` 

E você vai receber uma resposta formatada que se parece com essa:
```
+--------------------+
| Database           |
+--------------------+
| classicmodels      |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| test               |
+--------------------+
```
Onde temos uma tabela em cada linha é uma das databases que temos em nossa instância.

## Listar as Tabelas

Com o prompt ativo, use o comando SQL que já aprendemos `use` para acessar o Banco de Dados que você deseja usar e então use o comando a seguir para listar as tabelas presentes nele:
```
mysql> show tables;
```
E vamos ter um resultado formatado parecido com:
```
+-------------------------+
| Tables_in_classicmodels |
+-------------------------+
| customers               |
| employees               |
| offices                 |
| orderdetails            |
| orders                  |
| payments                |
| productlines            |
| products                |
+-------------------------+
```
Onde temos uma tabela em que cada linha é uma tabela em nosso Banco de Dados **classicmodels**.

## Ver a estrutura de uma tabela

Caso queira ver a estrutura de uma tabela pode usar o comando a seguir:
```
mysql> describe customers;
```
E vamos ter um retorno formatado como:
```
+--------------------+---------------+------+-----+---------+----------------+
| Field              | Type          | Null | Key | Default | Extra          |
+--------------------+---------------+------+-----+---------+----------------+
| id                 | int(11)       | NO   | PRI | NULL    | auto_increment |
| name               | varchar(100)  | NO   |     | NULL    |                |
| date_of_birth      | date          | NO   |     | NULL    |                |
+--------------------+---------------+------+-----+---------+----------------+
```
Em que vamos ter uma tabela com linhas e colunas nos indicando o nome do campo, o tipo, se ele aceita valores nulos, se ele é uma chave, qual o valor default e outras propriedades que ele possa ter como `auto_increment`.

## Dump do Banco de Dados

Para fazer uma cópia de uma base de dados que você tenha você pode usar o comando a seguir:
```
$ mysqldump -u root -p <nome da base de dados> > <nome da base de dados>.sql;
```
Por exemplo, para exportar o banco **classicmodels** usamos:
```
$ mysqldump -u root -p classicmodels > classicmodels.sql;
```

Isso vai nos gerar um arquivo **classicmodels.sql** na pasta em que nosso terminal está e que poderá ser usado para importar nosso banco com todas as tabelas e informações em qualquer outro computador que tenha o MySQL instalado pelo terminal ou por qualquer programa que importe arquivos .sql

## Importar o Banco de Dados

Para importar o arquivo .sql que foi exportado por você ou algum outro usuário você pode usar o comando a sequir, na pasta do terminal em que o arquivo .sql está:
```
mysql -u root -p <nome da base de dados> < <nome da base de dados>.sql;
```
Por exemplo, para importar o arquivo classicmodels.sql que exportamos o comando seria:
```
mysql -u root -p classicmodels < classicmodels.sql;
```

> O processo de importação pode demorar dependendo do tamanho de seu Banco de Dados. Quanto maior for, mais demorará. Por exemplo, um banco que tem 300.000 registro pode levar dezenas de minutos até concluir e liberar o terminal.

## Comandos SQL no terminal

Qualquer comando SQL que aprendemos no tutorial SQL4Noobs pode ser usada no terminal, seja `DROP`, `SELECT` ou qualquer outro. Após logar no terminal, entrar em Banco de Dados você pode executar por exemplo o comando `DROP` para apagar um Banco de Dados:
```
mysql> drop database products;
```
E pronto.

Caso queira usar um comando para manipular alguma tabela ou similar em um banco de dados primeiro você precisa primeiro usar o comando `use` para acessá-la e então executar qualquer comando por exemplo `SELECT`:
```
mysql> SELECT * FROM customers;
```
E isso vai nos dar um retorno formatado com o resultado dessa Query.

## Dicas
- Você pode usar o comando `CTRL+L` para limpar o terminal caso necessário.
- É necessário ter o mesmo cuidado ao usar comandos no Terminal quanto quando está os executando por interface gráfica, caso rode um comando que cause perda de dados isso vai ser um problema tão grave quanto seria por qualquer outro programa, mas o terminal não vai tentar te alertar sobre isso. Tenha cuidado.
