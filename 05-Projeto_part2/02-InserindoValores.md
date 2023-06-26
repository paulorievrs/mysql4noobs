# Inserindo valores

Lembrando que cada diciplina estará ligada a um único curso atravéz do codigocurso.

Observe:

```sql
INSERT INTO DISCIPLINA (codigodisciplina, nome, codigocurso)
    VALUES
(01, 'Compiladores', 01),--Ciência da Computação
(02, 'Banco de Dados I', 04), -- Eng.de Software
(03, 'Banco de Dados II', 04),-- Eng.de Software
(03, 'Cálculo 1', 03);-- Eng.da Computação
```

**Tabela DISCIPLINA:**
|codigodisciplina|nome             |codigocurso|
|----------------|-----------------|-----------|
|01              |Compiladores     |01         |
|02              |Banco de Dados I |04         |
|03              |Banco de Dados II|04         |
|04              |Cálculo 1        |03         |

Na próxima página vamos selecionar usando a chave estrangeira
<a href="./03-SelecionandoValores.md">Próximo -></a>