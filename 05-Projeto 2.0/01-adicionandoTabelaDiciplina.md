# Adicionando a tabela 'DISCIPLINA'

Vamos criar a tabela para conter as diciplinas do curso. Lembrando que uma disciplina vai pertencer a um curso, porém um curso poderá ter mais de uma disciplina.

Digite:

```sql
CREATE TABLE DISCIPLINA (
    codigodisciplina int NOT NULL,
    nome varchar(30) NOT NULL,
    codigocurso int NOT NULL,
    PRIMARY KEY (codigodisciplina),

    CONSTRAINT codigocurso
        FOREIGN KEY (codigocurso)
        REFERENCES CURSO(codigocurso)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);
```
Explicação:

**ON UPDATE CASCADE:** Indica um 'UPDATE em cascata', ou seja, quando atualizarmos o campo 'codigocurso' de algum registro da tabela 'CURSO', então o campo 'codigocurso' data tabela 'DICIPLINA' também será atualizado.

**ON DELETE CASCADE:** Indica um 'DELETE em cascata', ou seja, quando deletarmos algum registro da tabela 'CURSO', então todos os registros da tabela 'DICIPLINA' relacionados a este serão deletados também.

Na próxima página realizaremos inserções na tabela DISCIPLINAS


<a href="./02-InserindoValores.md">Próximo -></a>