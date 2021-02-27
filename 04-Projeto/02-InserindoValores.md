# Inserindo valores

Para começarmos a manipulação de dados devemos inserir valores em seus respectivos locais.

Como logicamente em uma faculdade, deve-se existir cursos para ter alunos, nada mais correto que inserirmos os cursos primeiramente do que os alunos.

## Cursos

Para inserirmos um curso, devemos utilizar o comando INSERT:

```sql
INSERT INTO CURSO (codigocurso, nomecurso) 
    VALUES
(01, 'Ciência da Computação');
```

Nesse caso inserimos o curso Ciência da Computação com seu respectivo código de curso 01.

Se você tiver vários dados é possível inserir vários com um comando como por exemplo:

```sql
INSERT INTO CURSO (codigocurso, nomecurso) 
    VALUES
(02, 'Analise e Desenvolvimento de Sistemas'),
(03, 'Engenharia da Computação'),
(04, 'Engenharia de Software'),
(05, 'Sistemas de Informação');
```

## Alunos

Como em cursos:

```sql
INSERT INTO ALUNO (matricula, nome, telefone, codigocurso)
    VALUES
(6334, 'Jose Neutro', '11999999999', 01);
```

Nesse caso, registramos o aluno Jose Neutro no Curso de Ciência da Computação utilizando seu código de curso.

Vamos inserir outros valores para manipula-los:

```sql
INSERT INTO ALUNO (matricula, nome, telefone, codigocurso)
    VALUES
(02, 'Jose Amazias', '11999999990', 02),
(03, 'Jose Oliveira', '11999999980', 03),
(04, 'Pedro Amazias', '11999999900', 03),
(05, 'Lucas Fernandes', '11999999970', 05),
(06, 'Paulo Oliveira', '11999999960', 04),
(07, 'Rodrigo Silva', '11999999770', 04),
(08, 'Gilberto Alous', '11999999550', 01),
(09, 'Daniel Reis', '11999999940', 02);
```
<a href="./03-SelecionandoValores.md">Próximo -></a>