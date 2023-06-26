# Alterando valores para

Agora, vamos realizar pequenas alterações nos nossos campos para treinarmos o comando UPDATE nas tabelas.

Vamos alterar o telefone de um aluno em específico:

```sql
UPDATE ALUNO SET telefone = '31999999999' WHERE matricula = 6334;
```

Com esse comando vocề altera o telefone aluno de matricula 6334 para  '31999999999'. Assim sem afetar os outros dados. Se não tivesse o comando WHERE seria alterado todos os telefone de todos os alunos.

Vamos alterar um nome de um curso:

```sql
UPDATE CURSO SET nomecurso = 'Ciências da computação' WHERE codigocurso = 1;
```
E se por acaso quisermos alterar um código de curso?

```sql
UPDATE CURSO SET codigocurso = 9999 WHERE codigocurso = 1;
```

Irá nós mostrar um erro, já que, o código curso já está sendo utiliizado em outra tabela, alterar campos e valores que são utilizados em relacionamentos sempre vai dar erro porque outros campos de outras tabelas dependem deeles.

<a href="./05-DeletandoValores.md">Próximo -></a>