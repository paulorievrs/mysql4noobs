# Selecionando valores

Vamos visualizar os valores inseridos com o comando SELECT.

Digite:

```SQL
SELECT * FROM CURSO;
```
Com esse comando você pode visualizar todos os cursos que foram inseridos.

```SQL
SELECT * FROM ALUNO;
```
Com esse comando você visualiza todos os alunos inseridos.

Mas geralmente para consultas são relizadas filtragens para melhor busca de dados.

Por exemplo:

```SQL 
SELECT nomecurso FROM CURSO WHERE nomecurso LIKE '%Sistemas%';
```
Nesse caso, buscamos somente o nomecurso da tabela CURSO aonde o nomecurso contém a string Sistemas em qualquer lugar, justamente pelo simbolo de porcentagem antes e atrás.

Nesse caso nos resultaria os nomes dos cursos de 'Analise e Desenvolvimento de Sistemas', 'Sistemas de Informação'.


Podemos também visualizar o registro de um aluno específico pelo seu número de matrícula:

```sql
SELECT * FROM ALUNO WHERE matricula = 6334;
```
Esse comando nós trás todos os dados do Aluno de matrícula 6334.

<a href="./04-AlterandoValores.md">Próximo -></a>