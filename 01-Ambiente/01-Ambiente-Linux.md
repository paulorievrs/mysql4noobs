# Ambiente Linux


## Instalação

A intalação no ambiente Linux (estou utilizando Ubuntu 20.04) como por padrão é via linha de comando, então abra seu terminal e bora.

Por padrão vamos atualizar seu sistema local. 

```
$ sudo apt update
```

E depois vamos instalar o mysql-server

```
$ sudo apt install mysql-server
```

Basicamente já está instalado o MySQL mas temos que configura-lo corretamente para melhor uso.

## Configuração

Execute o script de segurança, para isso precisamos de permissões de super usuário:

```
$ sudo mysql_secure_installation
```

Isso vai lhe fazer uma serie de perguntas, eu geralmente dou 'N' para ter pouca segurança na minha senha, já que vai ser somente um ambiente de desenvolvimento e aí você vai colocar uma senha, pode ser qualquer uma, se você quiser depois irei auxilia-lo a alterar.

Para entrar no MySQL você utilizaria:

```
$ mysql -u root -p
```
E ai digite sua senha para entrar e executar comandos.


Esses próximos passos são para alterar a senha senha ou remove-la, então se você quiser manter a senha que colocou no passo anterior pode já seguir para a <a href="../02-Introdução/01-Introducao.md">primeira página.</a>
## Autenticação

Execute o MySQL como super usuário:

```
$ sudo mysql
```

Agora dentro do MySQL utilize:

```sql
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password BY 'password';
```
Altere password pela sua senha preferência, se quiser pode deixar vazio.

E por fim utilize:

```sql
mysql> FLUSH PRIVILEGES;
mysql> exit;
```

Com isso está configurado seu MySQL e pode <a href="../02-Introdução/01-Introducao.md">seguir para o tutorial</a>