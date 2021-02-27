# Constraints

Como o nome já diz, pode ser traduzido literalmente para restrições para seu banco. Essas restrições podem ser definidas para gerar erros no banco e não ser salvos dados que não deveriam.


# UNIQUE

É utilizada essa constraint para definir essa valor como único, ou seja, se outro dado for inserido no banco, e nesse campo definido como UNIQUE estiver repitido, irá dar um erro e não irá inserir.

# NOT NULL

É utilizado para dizer que um campo não pode ser NULL, ou seja, não pode ser algo vazio, mas, lembre-se que vazio é diferente de uma string vazia.

# PRIMARY KEY

É utilizado para ser um dado único em cada registro. Nenhum outro registro pode ter uma PRIMARY KEY igual ou vazio. É a junção de UNIQUE e NOT NULL. 

# FOREIGN KEY

Diz que esse campo é de outra tabela, que relaciona geralmente a PRIMARY KEY de um registro de outra tabela, para assim gerar relacionamentos de bancos.

# CHECK

Define qual tipo tipo de valor deve estar nessa coluna, alguma retrição para isso, se por exemplo uma coluna puder receber só 3 tipos de valores, exemplo: ("SIM", "NÃO", "TALVEZ"), o CHECK cuida para que só possa ser inserido esses valores.

<a href="./03-ComandosBasicos.md">Próximo -></a>