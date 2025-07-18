# Desafio 3: Deployment de applicações para Azure

### Tempo Estimado: 60 Minutos

## Introdução

No desafio anterior, você desenvolveu com sucesso uma applicação: **MyMvcApp CRUD Application** totalmente funcional, principalmente com a assistência do **GitHub Copilot**, e também adquiriu conhecimento sobre como a IA pode ser integrada de forma eficiente ao fluxo de trabalho de desenvolvimento.

Como desenvolvedor de software na **Contoso Ltd.**, uma empresa líder em desenvolvimento de software, você foi designado para explorar tecnologias e ferramentas inovadoras que podem aprimorar o processo de desenvolvimento de software e a gestão da infraestrutura da empresa. A **Contoso Ltd.** reconhece o potencial da Infraestrutura como Código (IaC) na gestão e provisão de seus recursos de computação e está particularmente interessada em templates do Azure Resource Manager (ARM) para implantar aplicações no Azure.

Neste desafio, você utilizará o **GitHub Copilot** para otimizar o desenvolvimento de um template do **Azure Resource Manager (ARM)** para implantar a aplicação **MyMvcApp CRUD Application** totalmente funcional que você desenvolveu anteriormente. Os templates ARM são arquivos de Infraestrutura como Código (IaC) usados para implantar e gerenciar recursos no Azure. Aproveitando as capacidades de geração de código do Copilot, você acelerará a criação de um template ARM para implantar uma aplicação no Azure. Além disso, você também automatizará os processos de construção e teste do seu código. Você criará um pipeline do GitHub Actions, com o **GitHub Copilot** auxiliando na geração dos scripts necessários. Para documentar o conhecimento e as percepções adquiridas com este exercício, você usará o GitHub Copilot para gerar uma documentação abrangente e precisa para este desafio. Esta documentação servirá como um guia para a criação do template ARM, configuração do pipeline do GitHub Actions e implantação da **MyMvcApp CRUD Application** no Azure.

Ao concluir este desafio, você pretende demonstrar à Contoso Ltd. como o **GitHub Copilot** pode otimizar o desenvolvimento de templates ARM, automatizar processos de construção e teste com GitHub Actions e gerar uma documentação esclarecedora. Isso destacará ainda mais o valor da integração da IA no fluxo de trabalho de desenvolvimento, seguindo o desenvolvimento bem-sucedido da aplicação de banco de dados de contatos no desafio anterior.



## Pré-requisitos

Certifique-se de ter o seguinte no ambiente integrado fornecido pelo CloudLabs:

> **Observação:** Os pré-requisitos já estão configurados no ambiente fornecido pelo CloudLabs. Se você estiver usando seu computador pessoal ou laptop, certifique-se de que todos os pré-requisitos necessários estejam instalados para concluir este hackathon.

- [Visual Studio Code](https://code.visualstudio.com/)
- [Conta GitHub](https://github.com/)
- [Extensão GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) instalada no VS Code.
- Certifique-se de implantar o web app no grupo Resource Group existente com o nome **GitHub-Copilot-Challenges**.

## Aceder ao Azure Portal

1. Para acessar o portal do Azure, abra uma janela privada/incógnita no seu browser e navegue até **[Azure Portal](https://portal.azure.com)**.

1. Na aba **Sign in to Microsoft Azure**, você verá uma tela de login. Insira o seguinte e-mail/nome de usuário e clique **Next**. 
   * Email/Username: <inject key="AzureAdUserEmail"></inject>
        
1. Agora insira a seguinte senha e clique em **Sign in**.
   * Password: <inject key="AzureAdUserPassword"></inject>

1. **Ignore** o registro MFA se o pop-up aparecer enquanto faz login no portal do Azure.

1. Se você vir o pop-up **Stay Signed in?** clique em **Não**.

1. Se você vir o pop-up **You have free Azure Advisor recommendations!**, feche a janela para continuar o laboratório.

1. Se aparecer uma janela pop-up **Welcome to Microsoft Azure**, clique em **Cancel** para pular o tour.
   
1. Agora você verá o Painel do Portal do Azure. Clique em **Resource groups** no painel de navegação para ver os resource groups.
  
1. Confirme que você tem um resource group com o nome **GitHub-Copilot-Challenges** presente, conforme mostrado na captura de tela abaixo. Você precisará usar o resource group **GitHub-Copilot-Challenges** ao longo deste desafio.

## Challenge Objectives:

1. **Desenvolva um template ARM para implantar um aplicativo no Azure:**
   
   - Utilize o GitHub Copilot para ajudá-lo a gerar a estrutura inicial de um template ARM para implantar o **MyMvcApp CRUD Application** no Azure.
     
   - Defina os recursos necessários do Azure no template ARM, ou seja, uma **Web App** presente nos **Azure App Services** necessário para implantar a sua aplicação.
     
   - Salve os arquivos do template ARM e dos parâmetros no seu repositório do GitHub **MyMvcApp CRUD Application** como **deploy.json** e **deploy.parameters.json** no branch **master**.

   <validation step="93dbb711-57a3-462c-8ffe-699f1208865e" />

2. **Gerar um workflow de GitHub Action usando o Deployment Center de Azure App Service do portal do Azure:**
   
      - Implemente e construa o workflow através do **Deployment Center** da sua Web App usando o repositório de GitHub **MyMvcApp-Contact-Database-Application** para iniciar o pipeline que implantará a applicação em Azure.

         >**Observação:** A construção falhará devido ao caminho indefinido no seu arquivo YAML do workflow.
  
      - Especifique o caminho como **D:\a\MyMvcApp-Contact-Databse-Application\MyMvcApp-Contact-Databse-Application\bin\Release\net8.0\MyMvcApp** para os passos **dotnet publish** e **Upload artifact for deployment job** no seu workflow de GitHub Actions.

   <validation step="019351e9-84ff-4623-a26c-66afe706bf66" />

3. **Coloque a aplicação a funcionar no Azure:**
   
      - Verifique se a construção do pipeline do GitHub Actions foi bem-sucedida e se o aplicativo está funcionando conforme o esperado através da Web App.
  
         ![](../../media/challenge3-web-app-001.png)
     
      - Verifique se os recursos implantados correspondem às especificações descritas no seu template ARM e se o aplicativo está funcionando no **Default Domain** da Azure Web App.

4. **Gerar documentação com Copilot para o aplicativo:**
   
      - Utilize o GitHub Copilot para ajudar na geração de documentação detalhada e precisa especificamente para este desafio.
     
      - Crie um arquivo MD no seu repositório **MyMvcApp-Contact-Database-Application** no GitHub como um arquivo **README.md** na branch **master**. Este arquivo servirá como um guia para a criação do template ARM para implantar o aplicativo e o arquivo de fluxo de trabalho do pipeline do GitHub Actions.

## Critério de Sucesso:

- Verifique se a web app de Azure App Services contendo o código do seu aplicativo está presente no Azure.
- Verifique se o pipeline de Github action foi criado com sucesso.
- Verifique se o **MyMvcApp CRUD Application** foi implantado com sucesso no Azure e teste a funcionalidade.
- Verifique se a documentação foi criada com sucesso.

## Recursos adicionais:

- Consulte [aqui](https://learn.microsoft.com/en-us/azure/developer/github/deploy-to-azure) para ajuda adicional.
- Se você encontrar algum desafio ou tiver dúvidas, consulte a [Documentação do GitHub Copilot](https://github.com/github/copilot-docs) para obter orientações.

### Validação do Desafio

Forneca o username da conta de GitHub no formato **github-cloudlabsuser-XXXX** para o pass de validação **Validate GitHub directory**.

## Conclusão

Neste desafio, você demonstrou como a IA pode auxiliar significativamente no desenvolvimento e implementação de aplicações, especificamente através do uso do GitHub Copilot. Não apenas desenvolveu uma aplicação para aceder a um banco de dados de contatos totalmente funcional no desafio anterior, mas também a implementou de forma eficaz no Azure usando um ARM template gerado com a ajuda do GitHub Copilot. Você utilizou o GitHub Copilot para simplificar a criação do ARM template, que é um exemplo poderoso de Infraestrutura como Código (IaC), e também automatizou o processo de build e testes do seu código criando um pipeline do GitHub Actions, com o GitHub Copilot auxiliando na geração dos scripts necessários. Além disso, você produziu documentação abrangente e precisa para este desafio, servindo como um guia valioso para futuros projetos.

Através deste desafio, você demonstrou para a Contoso Ltd. o potencial de integrar a IA no fluxo de trabalho de desenvolvimento. Mostrou como o GitHub Copilot pode auxiliar não apenas no desenvolvimento de aplicações, mas também na implementação e gestão de infraestrutura, destacando assim sua versatilidade e valor. Ao implementar com sucesso a aplicação de acesso ao banco de dados de contatos no Azure e verificar sua funcionalidade, você forneceu uma demonstração tangível dos benefícios da IA no desenvolvimento de software.

### Clique em Avançar >> para prosseguir com o próximo desafio.

![](../../media/next-page-p.png)