# Desafio 2: Criar uma applicação com GitHub Copilot - Guia da Solução

## Task 1: Desenvolver a aplicação

### Login no GitHub

- Faça login no [GitHub](https://github.com/login) com a conta do GitHub fornecida pela CloudLabs. Certifique-se de que você está conectado à conta correta do GitHub fornecida para este laboratório.

### Faça um Fork do repositório

- Navegue até o link do repositório do GitHub fornecido: 
[MyMvcApp-Contact-Databse-Application](https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application.git).

    ![](../../media/Repo-info.png)

- Faça um fork do repositório para a conta do GitHub fornecida pelo CloudLabs.

    ![](../../media/Fork-repo.png)

### Abra o Visual Studio e Clone o Repositório

- Inicie o Visual Studio e clique em "Clone Git repository".

   ![](../../media/Clone-Git-repo.png)

- Insira a URL do repositório Git e pressione Enter.

    ![](../../media/URL-Repo.png)

- A janela ficará assim:

    ![](../../media/Cloned-rep.png)


### Configurando o Visual Studio 2022

- No Visual Studio, navegue e clique na opção **GitHub Copilot** localizada no canto superior direito e selecione **Install Copilot**.

- Na janela do Instalador do Visual Studio, certifique-se de que **GitHub Copilot** esteja selecionado e clique em **Install**. Isso fechará o Visual Studio.

- Aguarde até que a extensão GitHub Copilot seja baixada completamente (isso pode levar alguns minutos) e feche a janela do Instalador do Visual Studio.

  > **Observação:**  Ignore a mensagem de erro 'Couldn't install Microsoft.Net.4.8.1.FullRedist', isso não afetará os desafios.

- Reabra o Visual Studio e verifique se o GitHub Copilot está ativo. A janela de chat do GitHub Copilot agora pode ser utilizada.

- Uma vez que o repositório esteja clonado, localize e abra o arquivo `MyMvcApp.sln` no Solution Explorer.

  ![](../../media/MyMvcApp_ss.png)

- Navegue até Extensões 

  ![](../../media/Extension.png)

- Instale **Nuget Gallery** e **C# Dev Kit**

1. Clique em extensões no lado esquerdo
1. Procure por Nueget Gallery e C# Dev Kit
1. Clique em instalar.

    ![](../../media/NuGet.png) 
  
    ![](../../media/CAPP.png)

- Execute o comando abaixo na consola

    ```
    Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -r
    ```

    ![](../../media/crud5.6.png)

### Implemente Métodos usando o GitHub Copilot

- Navegue até ao arquivo `UserController.cs` na pasta `Controllers`.

    ![](../../media/crud2.7.png)

- Use o GitHub Copilot para gerar código para cada método vazio no arquivo `UserController.cs`. Para gerar código para cada método vazio usando o GitHub Copilot, selecione ou destaque as linhas do método vazio e, em seguida, clique com o botão direito nas linhas destacadas para abrir o menu de contexto.

    ![](../../media/crud1.2.png)

    ![](../../media/crud1.3.png)

- No menu de contexto, escolha a opção "Ask Copilot". Na caixa de prompt, digite "Fill in the Index method".

    ![](../../media/crud1.4.png)

- O GitHub Copilot gerará uma sugestão de código com base no contexto do método. Revise a sugestão fornecida pelo GitHub Copilot e você pode optar por aceitar ou descartar a sugestão com base em sua relevância para seus requisitos.

    ![](../../media/crud1.5.png)

- Repita esse processo para cada método vazio no arquivo UserController.cs até que todos os métodos estejam implementados.

- Seguir esses passos permitirá que você utilize o GitHub Copilot de forma eficiente para gerar código para cada método vazio no arquivo UserController.cs.

### Executar e testar a Aplicação

- Localize o botão do IIS Express button (um botão verde de play) na barra de ferramentas e clique nele. Essa ação inicia a aplicação no localhost num web browser.

    ![](../../media/crud1.6.png)

- Uma vez que você execute o aplicativo em um browser local através do IIS Express, alguns pop-ups aparecerão permitindo que a aplicação seja executada com um certificado self-signed gerado pelo IIS Express.

    ![](../../media/ssl-yes.png)

    ![](../../media/ssl-yes01.png)

### Criar um Novo Contato

- No browser aberto, localize o botão "Create New" e clique nele.

    ![](../../media/crud1.7.png)

- Preencha os campos obrigatórios para Name e Email no formulário fornecido. Clique no botão "Create" para enviar o formulário e criar um novo contato.

    ![](../../media/crud1.8.png)

### Editar um Contato

- Após criar um contato, retorne à página inicial.

- Encontre o contato que você criou na lista e localize o botão "Edit" associado a ele. Clique no botão "Edit".

    ![](../../media/crud1.9.png)

- Modifique os detalhes existentes (Name or Email) conforme desejado. Salve as alterações clicando no botão "Save".

    ![](../../media/crud1.10.png)

### Verificar Detalhes de um Contato

- Mais uma vez, retorne à página inicial.

- Localize o contato cujos detalhes você deseja verificar. Clique no botão "Details" associado a esse contato.

    ![](../../media/crud1.11.png)

- Verifique se os detalhes exibidos correspondem às informações que você inseriu anteriormente.

    ![](../../media/crud1.12.png)

### Apagar um Contato

- Na página inicial, encontre o contato que você deseja apagar.

- Clique no botão "Delete" associado a esse contato.

    ![](../../media/crud1.13.png)

- Uma caixa de diálogo de confirmação aparecerá perguntando se você tem certeza de que deseja apagar o contato. Confirme a ação.

    ![](../../media/crud1.14.png)

- Certifique-se de que o contato foi removido da lista.

    ![](../../media/crud1.15.png)

Seguindo estes passos meticulosamente, você poderá testar de forma completa as funcionalidades CRUD (Create, Read, Update, Delete) da aplicação e garantir seu funcionamento adequado.

# Task 2: Gerar scripts para teste unitários

- Para gerar casos de teste unitários, precisamos adicionar um novo projeto. No Solution Explorer, clique com o botão direito na Solução.

    ![](../../media/crud3.1.png)

- Clique em Add, e depois em New Project.

    ![](../../media/crud3.2.png)

- Agora, pesquise por Unit test na caixa de pesquisa, selecione Unit Test Project (.Net Framework)  e clique em Next.

    ![](../../media/crud3.3.png)

- Nomeie o projeto como Usercontrollertest e clique em Create.

    ![](../../media/crud3.4.png)

- Renomeie o arquivo UnitTest1.cs para UserControllerTests.cs.

- Agora vamos pedir ao GitHub Copilot Chat para gerar casos de teste. Clique na opção "View" no painel superior do Visual Studio. Nas opções, selecione "GitHub Copilot Chat" para abrir a janela do GitHub Copilot Chat.

    ![](../../media/crud3.5.png)

- Abra o arquivo UserController.cs e selecione/destaque todo o código nele.

    ![](../../media/crud3.6.png)

- Com todo o código destacado, no GitHub Copilot Chat, forneça o prompt "generate unit test cases for usercontroller.cs"

    ![](../../media/crud3.7.png)

- O GitHub Copilot começará a gerar casos de teste unitários para o usercontroller.cs.

    ![](../../media/crud3.8.png)

- Agora copie o código fornecido pelo GitHub Copilot clicando no ícone de copiar.

    ![](../../media/crud3.9.png)

- Remova o código existente e cole o código que copiamos no arquivo.

    ![](../../media/crud3.10.png)

- Agora vamos adicionar referências ao projeto. Localize References para UserControllertest e clique com o botão direito sobre elas. Em seguida, clique em Add Reference.

    ![](../../media/crud3.11.png)

- Na seção Projects, marque a caixa de seleção e clique em OK.

    ![](../../media/crud3.12.png)

- Agora vamos corrigir os problemas no arquivo passando o cursor sobre o Test Fixture e clicando nas opções Ask Copilot ou Quick Actions and Refactoring... (2) features.
  
    ![](../../media/ask-copilot.png)

    ![](../../media/quick-actions.png)

- Clique em "Install package NUnit" e depois em "Find and install latest version".

    ![](../../media/crud3.14.png)

- Da mesma forma, passe o cursor sobre controller.Index() clique em Show potential fixes, e depois em "Install package 'Microsoft.ASPNet.Mvc'" e clique em "Use Local version '5.2.7'"

    ![](../../media/crud3.15.png)

- Novamente, para RouteValues, passe o cursor e clique em click on show potential fixes, e depois clique em Add reference.

    ![](../../media/crud3.16.png)

- Novamente, para Assert, passe o cursor e clique em click on show potential fixes e depois clique em using Assert.

    ![](../../media/crud3.17.png)

- Após resolver todos os problemas no arquivo, clique na opção Test no painel superior do Visual Studio. Em seguida, clique em Test Explorer. 

    ![](../../media/crud3.18.png)

- No Test Explorer, clique no botão Run All para executar os casos de teste.

    ![](../../media/crud3.19.png)

- Verifique se todos os casos de teste foram aprovados.

    ![](../../media/crud3.20.png)

# Task 3: Desenvolver e testar funcionalidades

### Utilize o GitHub Copilot Chat para Desenvolvimento de Funcionalidades:
  
   - Clique na opção "View" no painel superior do Visual Studio. Nas opções, selecione "GitHub Copilot Chat" para abrir a janela do GitHub Copilot Chat.
  
        ![](../../media/crud3.5.png)

### Usar o GitHub Copilot Chat para Implementar Funcionalidades:
   
   - Inicie uma conversa com o GitHub Copilot Chat perguntando: "How can we add a search feature/functionality to our application?"

        ![](../../media/crud4.1.png)

   - Com base na resposta gerada pelo GitHub Copilot, prossiga com a implementação do código sugerido.
  
   - Neste caso, o GitHub Copilot sugeriu adicionar um novo método para aceitar uma string de busca como parâmetro e filtrar a lista de usuários com base na string de busca antes de passá-la para a view.

        ![](../../media/crud4.2.png)
  
   - Copie e cole o trecho de código fornecido no arquivo `UserController.cs` dentro do método na Action apropriado, geralmente o método `Index`. Neste código, se uma searchString for fornecida, a lista de usuários é filtrada para incluir apenas usuários cujos nomes contêm a searchString. Se nenhuma searchString for fornecida, todos os usuários são retornados.

        ```
        // GET: User
        public ActionResult Index(string searchString)
        {
            var users = from u in userlist
                        select u;
            if (!String.IsNullOrEmpty(searchString))
            {
                users = users.Where(s => s.Name.Contains(searchString));
            }
            return View(users.ToList());
        }
        ```

        ![](../../media/crud4.3.png)

   - O GitHub Copilot também sugeriu modificar o arquivo `Index.cshtml` localizado no caminho **Views\User\Index.cshtml** para incluir um formulário para a string de busca.

        ![](../../media/crud4.4.png)

   - Copie e cole o trecho de código fornecido no arquivo `Index.cshtml`. Este formulário envia um pedido GET para o método da Action Index, passando a string de busca como um parâmetro de query string.

        ```
        @using (Html.BeginForm("Index", "User", FormMethod.Get))
        {
            <p>
                Find by name: @Html.TextBox("searchString") 
                <input type="submit" value="Search" />
            </p>
        }
        ```

        ![](../../media/crud4.5.png)

### Salvar Alterações e Executar a Aplicação:

   - Salve os arquivos `UserController.cs` e `Index.cshtml` após fazer as alterações necessárias.

   - Execute o aplicativo clicando no botão do IIS Express. Essa ação inicia o aplicativo no localhost no seu browser.

        ![](../../media/crud1.6.png)

### Testar a Funcionalidade de Busca:

   - Adicione algumas entradas de contato ao aplicativo clicando no botão "Create New" e preenchendo os campos Name e Email.

        ![](../../media/crud4.6.png)

   - Após adicionar os contatos, teste a funcionalidade de busca digitando o nome de um contato no campo de busca que foi adicionado anteriormente. Clique no botão "Search" para executar a busca.

        ![](../../media/crud4.7.png)

   - Se a funcionalidade foi implementada corretamente, você deverá conseguir ver o contato pesquisado nos resultados.

        ![](../../media/crud4.8.png)

Seguindo esses passos, você poderá utilizar efetivamente o GitHub Copilot para implementar e testar novas funcionalidades na sua aplicação, aprimorando sua funcionalidade e usabilidade.

# Task 4: Gerar Mensagens de Commit

O novo recurso para gerar mensagens de Commit usa a IA do GitHub Copilot para descrever as alterações no seu código. Isso torna a escrita de mensagens de commit descritivas e úteis tão fácil quanto clicar em um botão e adicionar sua explicação.

- Localize Git Changes and e clique nele.

    ![](../../media/crud5.1.png)

- Use o novo ícone de caneta com brilho “Add AI Generated Commit Message” na janela Git Changes para gerar uma sugestão.

    ![](../../media/crud5.2.png)

- O GitHub Copilot analisará as alterações nos arquivos do seu commit, resumirá e descreverá cada mudança. Você pode então escolher “Insert AI Suggestion” ou “Discard”. Clique em Commit All.

    ![](../../media/crud5.3.png)

- Uma vez que o commit foi feito localmente, clique em Push para enviar as alterações para o repositório.

    ![](../../media/crud5.4.png)

### Clique em Avançar >> para prosseguir com o próximo desafio.

![](../../media/next-page-p.png)