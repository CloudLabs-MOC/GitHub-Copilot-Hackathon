# Desafio 2: Criar uma applicação com GitHub Copilot

### Tempo Estimado: 60 Minutos
  
## Introdução  

Na **Contoso Ltd.**, uma empresa líder em desenvolvimento de software, você, como **desenvolvedor de software**, recebeu a tarefa de explorar as capacidades do **GitHub Copilot**, um assistente de escrita de código baseado em IA, e aproveitá-las no processo de desenvolvimento de software da empresa. A empresa acredita que a integração da IA no processo de desenvolvimento pode aumentar significativamente a eficiência e a produtividade das equipes de desenvolvimento.

Como parte desta missão, você foi designado para desenvolver uma aplicação CRUD chamada **MyMvcApp** usando **GitHub Copilot**. O objetivo deste desafio é entender o potencial da IA no desenvolvimento de software e familiarizar-se com as capacidades do GitHub Copilot. Com a assistência do GitHub Copilot, você deverá gerar o código necessário, guiado pelos comentários fornecidos no arquivo. Você utilizará o GitHub Copilot em todas as etapas do processo de desenvolvimento, desde a geração de código para métodos vazios até a construção de recursos essenciais e o teste completo da aplicação.

Durante o desafio, você aproveitará a capacidade do Copilot de entender o contexto e fornecer sugestões de código relevantes. Ao interagir com o Copilot Chat, você melhorará a colaboração e receberá recomendações de escrita de código perspicazes, enriquecendo ainda mais sua experiência enquanto desenvolvedor.

Ao final deste desafio, seu objetivo é ter uma aplicação **MyMvcApp CRUD Application** totalmente funcional, desenvolvida principalmente com a assistência do **GitHub Copilot**. Após a conclusão, você não apenas terá desenvolvido uma aplicação rica em recursos, mas também terá adquirido valiosas percepções sobre como a IA pode ser integrada de forma contínua no fluxo de desenvolvimento. Esta experiência prática com o GitHub Copilot permitirá que você explore suas amplas capacidades e desbloqueie seu potencial em vários cenários de desenvolvimento. Isso demonstrará o potencial da IA no desenvolvimento de software e fornecerá valiosas percepções sobre sua implementação prática na **Contoso Ltd**.
  
## Pré-requisitos

Certifique-se de ter o seguinte no ambiente integrado fornecido pelo CloudLabs:

- Basic understanding of the C# programming language.  
- GitHub account.
- Crie uma pasta com o nome **GitHub Copilot** em **C:\Users\azureuser**.
- Execute os comandos abaixo no prompt de comando para criar uma nova pasta chamada **MyMvcApp.Tests** em **C:\Users\azureuser\GitHub Copilot** para gerar os unit test cases.

  ```
  cd "C:\Users\azureuser\GitHub Copilot"
  ```
  ```
  dotnet new xunit -n MyMvcApp.Tests
  ```

## Configurar o Visual Studio Code

1. Faça login no Visual Studio Code usando suas credenciais de usuário do GitHub a partir da tab **Environment > GitHub Credentials**.

2. Navegue até o link do GitHub abaixo e faça um fork do repositório para a conta GitHub fornecida pelo CloudLabs.

   ```
   https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application
   ```

   > **Nota:** Você já fez um fork do repositório GitHub fornecido no Desafio 01.
   
3. Clone o repositório em que anteriormente efetuou um fork no Visual Studio Code usando a conta GitHub fornecida pelo CloudLabs. 

4. No Visual Studio Code, localize a pasta **MyMvcApp.Tests** no Solution Explorer, clique com o botão direito e selecione **Open in integrated terminal**. Execute o comando abaixo no terminal para adicionar o pacote dotnet.

      ```
      dotnet add package Microsoft.CodeDom.Providers.DotNetCompilerPlatform
      ```

## Objectivos do Desafio  
1. **Desenvolver a aplicação:** 

      - Você criará uma aplicação CRUD chamada **MyMvcApp**, desenvolvida em C#, com a ajuda do **Github Copilot**, que permitirá aos usuários salvar os detalhes de contato das pessoas conforme os requisitos e realizar funções básicas como editar seus detalhes, excluir seus perfis, e assim por diante. Você receberá o esqueleto da aplicação já preparado, mas precisará implementar as funcionalidades dentro do arquivo **UserController.cs** por conta própria. Sua tarefa é completar esses métodos utilizando o GitHub Copilot para gerar o código necessário, guiado pelos comentários fornecidos no arquivo.

      - Explore a capacidade do Copilot de entender seu contexto e fornecer sugestões de código relevantes..
        >**Dica:** Utilize os recursos **Start in Editor**, **Fix** e **GitHub Copilot chat** do GitHub Copilot para desenvolver o código necessário.

      - Teste a aplicação minuciosamente e garanta que todas as funcionalidades estejam funcionando conforme o esperado.
  
        ![](../../media/challenge3-mymvcapp-localhost.png)

   <validation step="daaa3f6f-00f1-437a-8f35-01b59fb2da41" />

   <validation step="c7f107a0-97a2-4442-9cef-b14297fd5b7a" />

2. **Gerar scripts para teste unitários e validação de testes**:

      - Para cada uma das funcionalidades no **MyMvcApp** que você desenvolveu no arquivo **UserController.cs**, gere casos de teste unitários para o arquivo **UserControllerTests.cs** utilizando **xunit** com a ajuda do **Github Copilot**.
        >**Dica:** Renomeie o arquivo **UnitTest1.cs** para **UserControllerTests.cs** após criar a pasta **MyMvcApp.Test**.

      - Execute os scripts necessários gerados pelo **Github Copilot** e verifique se todos os casos de teste unitários foram aprovados.

3. **Desenvolver e testar funcionalidades:** 

      - Após completar os métodos, o próximo passo é desenvolver e adicionar uma funcionalidade de busca à aplicação e testar esta funcionalidade de forma minuciosa.
        
      - Utilize o GitHub Copilot para gerar trechos de código para a construção da funcionalidade de busca.

      - Teste a aplicação e certifique-se de que a funcionalidade de busca está funcionando conforme esperado.
  
        ![](../../media/challenge3-mymvcapp-search.png)

4. **Use o GitHub Copilot em cada etapa do desafio:** 

      - Utilize o GitHub Copilot para ajudar a escrever mensagens de commit significativas que descrevam claramente as alterações realizadas.

      - Ao longo do processo de desenvolvimento, interaja com o Copilot Chat para melhorar a colaboração e receber recomendações de código interessantes.
  
## Critério de Sucesso  

- Verifique se os métodos no arquivo `UserController.cs` foram concluídos com sucesso usando o GitHub Copilot.
- Verifique se todos os casos de teste gerados pelo Copilot passaram.
- Verifique se o recurso de pesquisa desenvolvido está funcionando conforme o esperado.
- Certifique-se de utilizar com sucesso o GitHub Copilot para escrever mensagens de commit.

## Recursos Adicionais:

- Consulte a [Documentação do GitHub Copilot](https://github.com/github/copilot-docs) para esclarecimentos durante a execução do desafio.
  
### Validação do Desafio

Forneca o username da conta de GitHub no formato **github-cloudlabsuser-XXXX** para o pass de validação **Validate GitHub directory**.

## Conclusão  
Neste desafio, você conseguiu desenvolver uma aplicação de para aceder a um banco de dados de contatos totalmente funcional, predominantemente com a assistência do GitHub Copilot, demonstrando sua utilidade prática em um cenário real de desenvolvimento de software.
Você navegou com sucesso pelo processo de desenvolvimento, desde a geração de código para métodos vazios no arquivo UserController.cs até a construção de recursos essenciais para a aplicação. Você utilizou o GitHub Copilot para entender o seu contexto e fornecer sugestões de código relevantes, aprimorando sua experiência de escrita de código.

O envolvimento com o Copilot Chat enriqueceu sua colaboração e forneceu recomendações de código perspicazes, mostrando como a IA pode ser integrada de forma fluida no fluxo de trabalho de desenvolvimento. Os casos de teste gerados com a assistência do GitHub Copilot garantiram a robustez e a confiabilidade da sua aplicação. Suas conquistas neste desafio demonstraram o potencial da IA no desenvolvimento de software e forneceram valiosas percepções sobre sua implementação prática. Você mostrou que, com as ferramentas certas, como o GitHub Copilot, o processo de desenvolvimento pode ser mais eficiente e produtivo.

### Clique em Avançar >> para prosseguir com o próximo desafio.

![](../../media/next-page-p.png)