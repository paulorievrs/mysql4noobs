# Ambiente Windows

1. Em primeiro lugar acesse o [site oficial do MySQL](https://mysql.com) 

<img src="../assets/win01.png">

2. Vá em Downloads

<img src="../assets/win02.png">


3. Desça a tela ate achar o link do MySQL Commumity

<img src="../assets/win03.png">

4. Clique em MySQL Installer for Windows

<img src="../assets/win04.png">

5. Baixe o Windows (x86, 32-bit), MSI Installer - (mysql-installer-community-8.0.23.0.msi)

<img src="../assets/win05.png">

6. Clique para realizar o download sem login/cadastro.

<img src="../assets/win06.png">

7. Execute o instalador como administrador e marque a opção para ceitar os termos e dê next.

<img src="../assets/win07.png">


8. Agoora selecione o padrão para desenvolvedor

<img src="../assets/win08.png">

9. Agora ele vai verificar se seu sistema tem os requisítos necessários para baixar o MySQL e suas dependências. Clique em execute. Instale os pacostes/programas que ele requerir.

<img src="../assets/win09.png">

10. Se ele mostrar uma caixinha perguntando se você quer continuar pois alguns requisitos não foram instalados corretamente, clique em "yes" para prosseguir.

<img src="../assets/win10.png">

11. Agora ela irá te mostrar quais softwares/pacotes serão baixados efetivamente para funcionar o nosso banco de dados. Clique em execute.

<img src="../assets/win11.png">

12. Agora clique em next

<img src="../assets/win12.png">

13. Na próxima tela, é só prosseguir com nextm deixando marcado "Standalone MySQL Server / Classic MySQL Replication"

<img src="../assets/win13.png">

14. Nessa tela são configurações de como irá ser feito a comunicação com o banco. Tome cuidado que se você tiver algum serviço rodando na porta 3306 irá conflitar com o MySQL, mas se não souber algum fique tranquilo e pode prosseguir em next.

<img src="../assets/win14.png">

15. Agora, são métodos de autenticação, você pode deixar a primeira opção selecionada e clicar em next.

<img src="../assets/win15.png">

16. Agora é sua parte de configurações de senha, você deve lembrar dessa senha depois e se ele disser que sua senha é fraca não tem problema, levando em conta que esse servidor é somente para testes e desenvolvimento. Após colocar a senha clique em next.

<img src="../assets/win16.png">

17. Nessa tela é só como o MySQL será executado e como irá ocorrer o gerenciamento. Por padrão pode deixar tudo como está e clicar em next.

<img src="../assets/win17.png">

18. Nessa tela você pode clicar em execute e executar o que foi definido. E após isso clique em finish.

<img src="../assets/win18.png">


19. Agora é clicar next para executar as configurações que faltam.


<img src="../assets/win19.png">

20. Só clicar em finish para deixar como padrão.

<img src="../assets/win20.png">

21. Voltaremos a tela de configuração e clique em next novamente.

<img src="../assets/win21.png">

22. Testaremos a configuração com o servidor com seu nome de usuário e senha definidos. Por padrão o nosso usuário principal é o root. Coloque sua senha definida anteriormente e clique check.

Se ficar como abaixo está configurado e pronto para uso seu MySQL

<img src="../assets/win22.png">

23. Clique em execute, e após finalizar clique em finish.

<img src="../assets/win23.png">

24. Clique em next.

25. Clique em finish desmarcando a opção do Shell.
<img src="../assets/win24.png">

26. Quando abrir o MySQL Workbench você clique em Local instance MySQL80 como abaixo:

<img src="../assets/win25.png">

27. Insira sua senha, e se quiser que fique salvo marque a caixinha abaixo do campo de texto e clique em OK.

<img src="../assets/win26.png">

28. Agora você está dentro do seu banco de dados e há um editor de texto para você executar seus comandos SQL. Você pode testar um comando digitando:

```sql
SHOW DATABASES
```
E teclando SHIFT + ENTER;

Com isso irá aparecer os banco de dados já existentes e criados por padrão pelo MySQL. Você pode seguir para <a href="../02-Introdução/01-Introducao.md">primeira página.</a>