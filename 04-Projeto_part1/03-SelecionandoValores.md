# Selecionando valores

Vamos visualizar os valores inseridos com o comando SELECT.

Digite:

```SQL
SELECT * FROM CURSO;
```

**RESPOSTA DA QUERY:**
|codigocurso|nomecurso                            |
|-----------|-------------------------------------|
|01         |Ciência da Computação|
|02         |Analise e Desenvolvimento de Sistemas|
|03         |Engenharia da Computação|
|04         |Engenharia de Software|
|05         |Sistemas da Informação|
<br>

Com esse comando você pode visualizar todos os cursos que foram inseridos.

```SQL
SELECT * FROM ALUNO;
```
**Tabela ALUNO:**
|matricula|nome           |telefone   |codigocurso|
|---------|---------------|-----------|-----------|
|01       |Jose Neutro    |11999999999|01         |
|02       |Jose Amazias   |11999999990|02         |
|03       |Jose Oliveira  |11999999980|03         |
|04       |Pedro Amazias  |11999999900|03         |
|05       |Lucas Fernandes|11999999970|05         |
|06       |Paulo Oliveira |11999999960|04         |
|07       |Rodrigo Silva  |11999999770|04         |
|08       |Gilberto Alous |11999999550|01         |
|09       |Daniel Reis    |11999999940|02         |
<br>


Com esse comando você visualiza todos os alunos inseridos.

Mas geralmente para consultas são relizadas filtragens para melhor busca de dados.

Por exemplo:

```SQL 
SELECT nomecurso FROM CURSO WHERE nomecurso LIKE '%Sistemas%';
```
**RESPOSTA DA QUERY:**
|codigocurso|nomecurso                            |
|-----------|-------------------------------------|
|02         |Analise e Desenvolvimento de Sistemas|
|05         |Sistemas da Informação|
<br>


Nesse caso, buscamos somente o nomecurso da tabela CURSO aonde o nomecurso contém a string Sistemas em qualquer lugar, justamente pelo simbolo de porcentagem antes e atrás.

Nesse caso nos resultaria os nomes dos cursos de 'Analise e Desenvolvimento de Sistemas', 'Sistemas de Informação'.


Podemos também visualizar o registro de um aluno específico pelo seu número de matrícula:

```sql
SELECT * FROM ALUNO WHERE matricula = 01;
```

**RESPOSTA DA QUERY:**
|matricula|nome           |telefone   |codigocurso|
|---------|---------------|-----------|-----------|
|01       |Jose Neutro    |11999999999|01         |
<br>

Esse comando nós trás todos os dados do Aluno de matrícula 01.

<a href="./04-AlterandoValores.md">Próximo -></a>