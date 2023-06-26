# Selecionando valores

Vamos começar com uma seleção um pouco mais complexa. Portanto, para simplificar a consulta usaremos o comando **'as'** para dar um apelido para as nossas colunas. ALUNO -> A e CURSO -> C.

Digite:

```SQL
SELECT A.nome, C.nomecurso
FROM ALUNO as A, CURSO as C
WHERE A.codigocurso = C.codigocurso;
```
Com o comando acima você pode visualizar duas colunas, uma para os alunos e outra para os cursos.

Na próxima página vamos deletar algusn registros

<a href="./04-AlterandoValores.md">Próximo -></a>