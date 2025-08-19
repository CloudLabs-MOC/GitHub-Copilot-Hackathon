# Desafio 4: Utilizando o workspace e a referência a arquivos do GitHub Copilot - Guia da Solução

>**Observação:** Os resultados produzidos pelo **GitHub Copilot** para esta tarefa específica podem não se alinhar precisamente com os seus. Essa discrepância ocorre porque o **GitHub Copilot** é uma ferramenta impulsionada por IA que pode gerar resultados variáveis de tempos em tempos.

### Tarefa 1: Utilizar o GitHub Copilot Workspace

Nesta tarefa, você utilizará o GitHub Copilot Workspace para aumentar a eficiência na escrita de código, fornecendo sugestões de código contextualmente relevantes.

1. Abra seu projeto no VS Code, onde você está logado(a) usando as credenciais do GitHub fornecidas pela CloudLabs.

    ![](../../media/vscode-launch.png)

1. Ao lado da barra de pesquisa, selecione o ícone do **Copilot**. Você verá a janela de boas-vindas do chat do **GitHub Copilot**.

    ![](../../media/file1.png)

1. Na caixa de texto, digite **@** e selecione **Workspace** para começar a trabalhar com o agente do **GitHub Copilot Workspace**.

    ![](../../media/file2.png)

1. Agora, você pode fornecer seus próprios comandos e selecionar **Enviar** para obter a resposta. Para começar, você pode perguntar ao **GitHub Copilot Chat** como iniciar seu projeto atual, fornecendo o seguinte comando: `How do I start the current project?`. Ao enviar seu prompt, o Copilot analisará automaticamente os arquivos e diretórios do workspace atual, dividido em etapas:

    1. Examina os nomes dos arquivos ou diretórios para entender quais são potencialmente relevantes para fornecer uma resposta.

    1. Leia o conteúdo dos arquivos. Às vezes, o arquivo inteiro, outras vezes apenas partes dele (devido aos limites de memória de tokens).

    1. Cria contexto a partir de tudo o que conseguiu coletar.

    1. Começa a responder, combinando o contexto do prompt com o que conseguiu obter.

    ![](../../media/file3.png)

1. O **GitHub Copilot** fornecerá uma explicação passo a passo de como executar seu projeto. Você pode seguir os mesmos passos e verificar se seu projeto está rodando com sucesso.

    ![](../../media/file4.png)

1. Além disso, você também pode executar o comando `Tell me the current workspace structure.` sem a ajuda do **agente do Workspace**, e comparar os resultados.

    ![](../../media/file5.png)

    A resposta fornecida é extremamente abstrata e, no final, informa que não pode fornecer a solução exata e gera apenas uma solução genérica.
 
1. Depois disso, você pode tentar o prompt usando a funcionalidade **Workspace** e obter informações completas sobre o seu projeto atual, fornecendo o seguinte prompt: `@workspace Tell me about the current workspace structure.`

    ![](../../media/file6.png)

    Analise a saída gerada e verifique se a estrutura está alinhada com a estrutura real do seu projeto. 

1. Você também pode experimentar os seguintes prompts de exemplo, fornecer seus próprios prompts conforme sua curiosidade e requisitos, e verificar o resultado:

    ```
    @workspace Create a new lazy-loaded page with the path “/faq.”
    ```
    ```
    @workspace How can I add a new route to my ASP.NET MVC application?
    ```
    ```
    @workspace How can I handle form submissions in ASP.NET MVC?
    ```
    
### Tarefa 2: Utilizando o GitHub Copilot Workspace para Criar um Novo Workspace de Aplicação

O GitHub Copilot Workspace não apenas fornece instruções, respostas ou trechos de código detalhados para as consultas que você envia, mas também pode criar o workspace completo de uma aplicação do zero. Aqui, você criará um novo aplicativo React simples chamado **Expense Tracker** para rastrear as despesas dos usuários e também modificá-las (editar) ou excluí-las, tudo com a ajuda do **GitHub Copilot workspace**. Você depurará o aplicativo usando este mesmo recurso e verificará se ele é executado com sucesso em seu ambiente local. Para criar o aplicativo `Expense Tracker` usando o **GitHub Copilot workspace**, siga os passos abaixo:

1. Crie uma nova pasta chamada **DemoApp** em **C:/Users/azureuser**.

1. Abra uma nova janela no **VS code** escolhendo **Arquivo** na barra superior e, em seguida, selecionando **Nova Janela**.

    ![](../../media/new-window.png)

1. Agora, selecione **Abrir Pasta** na página de **Boas-vindas**, navegue até a pasta **C:\Users\azureuser\DemoApp** e clique duas vezes para abri-la no seu VS Code.

    ![](../../media/vscode-open-folder.png)

1. No painel esquerdo, selecione o ícone de **Chat**. Você será a janela de boas-vindas do **Github Copilot** .

    ![](../../media/vscode-copilot-chat.png)

1. Na caixa de texto, digite **@** e selecione **Workspace** para começar a trabalhar com o agente do **Github Copilot Workspace**.

    ![](../../media/@workspace.png)

1. Forneça o prompt, **Create a workspace for the Expense Tracker React application with all the necessary files and code**. Na caixa de texto, selecione **Enviar** para gerar o workspace completo da sua aplicação React Rastreador de Despesas, juntamente com alguns arquivos de componentes.

    ![](../../media/expense-tracker-workspace.png)

    >**Observação:** A versão atual do **Github Copilot Workspace** permite criar o workspace automaticamente com toda a estrutura de arquivos; basta clicar em **Criar Workspace**.

1. Agora, crie o workspace para sua aplicação **Expense Tracker** criando os arquivos e pastas necessários. Para fazer isso, selecione **Explorador** no painel esquerdo e escolha os ícones apropriados de arquivo ou pasta para criar um novo arquivo ou pasta conforme a estrutura do workspace da sua aplicação.

    ![](../../media/vscode-explorer.png)

1. A estrutura do workspace para sua aplicação **Expense Tracker** será semelhante a esta, conforme a saída gerada pelo **GitHub Copilot Workspace**:

    ![](../../media/created-workspace.png)

1. Agora, gere o código para todos os componentes necessários da sua aplicação fornecendo os prompts relevantes ao **GitHub Copilot** na seção de **Chat**. Por exemplo, para criar o código para o componente **ExpenseForm.js** da sua aplicação, escreva `@workspace. How can I add functionality to the ExpenseForm component to handle user input and save expenses?` e selecione **Enviar**.

    O **GitHub Copilot** fornecerá o código relacionado ao componente referenciado.

    ![](../../media/expense-form.png)

1. Selecione o ícone **Copiar** para copiar o código e cole-o no componente **ExpenseForm.js** correspondente. Salve o arquivo.

    ![](../../media/expense-form-completed.png)

    >**Observação:** Leia a saída gerada pelo **Copilot** com atenção e certifique-se de instalar todos os pacotes necessários, se solicitado pelo Copilot, antes de executar sua aplicação.

1. Faça o mesmo para todos os componentes necessários da sua aplicação sugeridos pelo **GitHub Copilot Workspace** no **GitHub Copilot Chat**, e complete todos os componentes.

1. Certifique-se de utilizar o **GitHub Copilot Workspace** em caso de qualquer erro em algum dos componentes da sua aplicação. Por exemplo, se um problema aparecer no arquivo **app.js** da sua aplicação, você pode fornecer um prompt semelhante ao dado para descobrir a causa do erro e usar as capacidades avançadas do **GitHub Copilot Workspace** para corrigir o erro: `@workspace. Fix the issue in the app.js file.`

    >**Observação:** Certifique-se de usar o comando **@workspace** na caixa de chat para utilizar o recurso de workspace, para que ele possa analisar todos os arquivos e diretórios do seu workspace e fornecer a melhor solução para o erro que não entre em conflito com nenhum outro componente.

1. Você obterá um resultado semelhante a este:

    ![](../../media/error-fix.png)

    Analise a resposta e resolva os erros usando os passos fornecidos nela.

1. Após corrigir todos os erros, digite o prompt `@workspace. How can I run this app?` no Copilot e envie a solicitação para obter as instruções de execução da aplicação.

    Siga os passos fornecidos e execute sua aplicação.

    ![](../../media/run-app.png)

1. Você também pode verificar se todos os pré-requisitos necessários para executar seu aplicativo **Expense Tracker** já estão instalados, fornecendo ao Copilot o prompt `@workspace. What are the prerequisites I should install to run this app?`
    ![](../../media/app-prerequisites.png)

    Revise atentamente a resposta gerada pelo **GitHub Copilot** usando sua funcionalidade de workspace e certifique-se de que todos esses pré-requisitos estão instalados. Caso contrário, instale-os seguindo os passos mencionados na resposta.

1. Execute a aplicação, e ela abrirá no seu navegador **Edge** como mostrado abaixo:

    ![](../../media/app-working.png)

### Tarefa 3: Utilizar as Capacidades de Referência a Arquivos

**Referência a Arquivos no GitHub Copilot** refere-se à capacidade da IA de entender e interpretar o contexto do seu projeto considerando as informações contidas em outros arquivos dentro do seu workspace.

Quando você está trabalhando em um arquivo específico no seu código, o **GitHub Copilot** pode levar em consideração as informações, funções, classes ou variáveis definidas em outros arquivos do seu projeto. Isso significa que ele não fornece apenas sugestões com base no arquivo atual em que você está trabalhando; ele também pode referenciar outros arquivos para oferecer conclusões de código mais precisas e relevantes. Essa funcionalidade é particularmente útil quando você está trabalhando em grandes projetos onde o código está distribuído por vários arquivos. A capacidade do **GitHub Copilot** de referenciar outros arquivos permite que ele entenda melhor o panorama geral do seu projeto, resultando em sugestões mais contextualizadas. Isso pode melhorar significativamente sua eficiência de codificação e a qualidade geral do seu código.

Nesta tarefa, você utilizará a capacidade de **Referência a Arquivos do GitHub Copilot** para aprimorar a eficiência da codificação. Para usar o recurso de Referência a Arquivos, siga os passos abaixo:

1. Abra o seu projeto **Expense Tracker** no **VS Code**, onde você está logado(a) usando os detalhes da conta do GitHub fornecidos pela CloudLabs.

    ![](../../media/vscode-launch.png)

1. No painel à esquerda, selecione o ícone de **Chat**. Você verá a janela de boas-vindas do **GitHub Copilot**.

    ![](../../media/vscode-copilot-chat.png)

1. Na caixa de texto, digite **@** e selecione **Workspace** para ativar o agente do **GitHub Copilot Workspace**. Você precisará desse agente para analisar todo o seu workspace, para que ele possa fornecer respostas precisas e os blocos de código relacionados, referenciando os arquivos corretos.

    ![](../../media/@workspace.png)

1. Agora, você pode usar o seguinte prompt para entender como a funcionalidade de referência de arquivos funciona no **GitHub Copilot**. Ele pode fornecer uma resposta precisa para o arquivo ao qual você faz referência:: `What is the purpose of the index.js file in my project?`

    O **GitHub Copilot** fará referência às informações, funções, classes ou variáveis definidas no arquivo sobre o qual você fez a pergunta e fornecerá uma explicação detalhada do que está no **index.js**. Não apenas a explicação; ele também fornecerá o código relacionado acompanhado da resposta, referenciado no arquivo fornecido.

    O **GitHub Copilot** também referencia automaticamente os arquivos adicionais em seu projeto que podem ser necessários para fornecer a melhor resposta. Para obter informações sobre esses arquivos, selecione **Usou n referências** (onde **n** é o número total de arquivos referenciados do seu projeto atual) presente no início da resposta e veja todos os arquivos que o **GitHub Copilot** referenciou para fornecer a resposta.

    ![](../../media/files-referred-2.png)

    Alguns outros prompts que você pode fornecer para entender o recurso de referência a arquivos são:

    ```
    @workspace What does the ExpenseList.js file do in my application?
    ```
    ```
    @workspace What is the purpose of the app.js file in my project?
    ```
    ```
    @workspace How can I change the CSS for my application?
    ```
    
#### **Adicionando um novo recurso na aplicação usando Referência a Arquivos:**

Nesta tarefa, você utilizará a capacidade de referência de arquivos para integrar um novo recurso em sua aplicação **Expense Tracker**. Você incluirá um campo **Date** no documento **ExpenseForm** e exibirá essa data no **ExpenseItem**, permitindo que você classifique as despesas por data no componente **ExpenseList**.

Para fazer isso, siga os passos abaixo:

1. Abra seu projeto no VS Code, onde você está logado(a) usando os detalhes da conta do GitHub fornecidos pela CloudLabs.

    ![](../../media/vscode-launch.png)

1. No painel à esquerda, selecione o ícone de **Chat**. Você verá a janela de boas-vindas do **GitHub Copilot**.

    ![](../../media/vscode-copilot-chat.png)

1. Na caixa de texto, digite **@** e selecione **Workspace** para ativar o agente do **GitHub Copilot Workspace**. Você precisará desse agente para analisar todo o seu workspace, para que ele possa fornecer respostas precisas e os blocos de código relacionados, referenciando os arquivos corretos.

    ![](../../media/@workspace.png)

1. Agora, forneça o seguinte prompt para incluir um novo campo **Date** nos componentes e permitir que os usuários classifiquem suas despesas conforme necessário: `How can I modify the ExpenseForm component to include a date field, display this date in the ExpenseItem component, and sort the expenses by date in the ExpenseList component?`

1. A funcionalidade do **GitHub Copilot**  fará referência aos arquivos que você mencionou nos prompts, bem como analisará todo o seu workspace e fornecerá a melhor resposta possível. Ele fornecerá os trechos de código que você pode adicionar aos componentes **ExpenseForm**, **ExpenseItem**, e **ExpenseList** de acordo. Você também pode visualizar os arquivos que foram referenciados ao fornecer a resposta, selecionando **Usou n references** (onde n é o número de arquivos referenciados) presente no início da resposta.

    ![](../../media/files-referred.png)

1. Você pode analisar a resposta, fazer as alterações sugeridas pelo **GitHub Copilot** usando sua funcionalidade de referência de arquivos e editar os componentes conforme fornecido na resposta.

1. Execute o aplicativo e verifique se o componente **Date** foi adicionado e está funcionando corretamente.

    ![](../../media/app-working-date.png)

## Conclusão

Neste desafio, você obteve uma compreensão mais profunda de como o **GitHub Copilot Workspace** e a **Referência a Arquivos** funcionam e como eles podem aprimorar seu processo de codificação. Ao usar eficazmente esses recursos, você pode melhorar significativamente sua eficiência de programação e a qualidade geral do seu código. Seja você um(a) desenvolvedor(a) experiente ou iniciante, esses insights certamente serão valiosos em sua jornada de programação.

### Clique em Avançar >> para prosseguir com o próximo desafio.

![](../../media/next-page-p.png)
