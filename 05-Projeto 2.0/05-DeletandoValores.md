# Deletando Valores

Agora vamos deletar um curso da tabela 'CURSO' para ver o que acontece.

**Tabela CURSO:**
|codigocurso|nomecurso                            |
|-----------|-------------------------------------|
|01         |Ciência da Computação|
|02         |Analise e Desenvolvimento de Sistemas|
|03         |Engenharia da Computação|
|04         |Engenharia de Software|
|05         |Sistemas da Informação|
<br>


```sql
DELETE FROM CURSO WHERE codigocurso = 04;
```

**Tabela CURSO:**
|codigocurso|nomecurso                            |
|-----------|-------------------------------------|
|01         |Ciência da Computação|
|02         |Analise e Desenvolvimento de Sistemas|
|03         |Engenharia da Computação|
|05         |Sistemas da Informação|
<br>

É possivel notar que não temos mais a disciplina de Engenharia de Software. Vamos olhar agora a tabela 'DISCIPLINA'.

**Tabela DISCIPLINA:**
|codigodisciplina|nome             |codigocurso|
|----------------|-----------------|-----------|
|01              |Compiladores     |01         |
|04              |Cálculo 1        |03         |
<br>

Perceba que todas as disciplinas de Banco de Dados I e II, também foram deletadas. Isso se deve ao comando que inserimos na criação da tabela 'DISCIPLINA' o 'ON DELETE CASCADE'. Mas, será que a tabela 'ALUNO' também foi afetada?

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

Lembre que usamos o comando 'ON DELETE NO ACTION', portanto quando deletamos o registro da tabela outra tabela, nada foi feito nesta.

<a href="./06-ConsideracoesFinais.md">Proximo -></a>