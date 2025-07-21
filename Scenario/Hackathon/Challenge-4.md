# Desafio 4: Usar GitHub Copilot workspace and referêencia a arquivos

### Tempo Estimado: 60 Minutos

## Introdução

Como desenvolvedor de software na **Contoso Ltd.**, uma empresa líder em desenvolvimento de software, você está sempre buscando formas de melhorar sua eficiência na escrita de código e a qualidade geral do seu código. Após explorar com sucesso os recursos básicos do **GitHub Copilot** e utilizá-lo para desenvolver e implantar uma aplicação no Azure, você agora direciona seu foco para alguns dos recursos avançados deste assistente de escrita de código com IA.

Neste desafio, sua tarefa é explorar e utilizar três recursos-chave do **GitHub Copilot**: o **workspace** e o **file reference**. Compreender e utilizar esses recursos pode aumentar significativamente sua produtividade e eficiência na escrita de código, proporcionando sugestões de código mais precisas e contextualizadas.

- **GitHub Copilot Workspace:** **GitHub Copilot Workspace** é uma funcionalidade avançada do **GitHub Copilot**, uma ferramenta de autocompletação de código com IA. O workspace no GitHub Copilot se refere ao diretório de trabalho atual onde seus arquivos de código estão localizados.

   Quando você está a escreve código, o **GitHub Copilot** utiliza as informações do seu workspace para gerar sugestões de código contextualmente relevantes. Isso significa que ele leva em consideração os detalhes do seu projeto atual, como os arquivos de código, bibliotecas e dependências presentes no seu workspace, para fornecer as autocompleções de código mais adequadas. Esse recurso torna o **GitHub Copilot** um assistente de escrita de código inteligente, que não só entende a sintaxe e a semântica da linguagem, mas também o contexto do seu projeto, resultando em sugestões de código mais precisas e úteis.
   Ao usar o recurso **Workspace** de forma eficaz, os desenvolvedores podem melhorar sua eficiência na escrita de código, reduzir erros e criar códigos de maior qualidade.

- **File referencing in GitHub Copilot:** **File referencing in GitHub Copilot** refere-se à capacidade da IA de entender e interpretar o contexto do seu projeto, considerando as informações em outros arquivos dentro do seu workspace.

   Quando você está trabalhando em um arquivo específico do seu código, o **GitHub Copilot** pode levar em consideração as informações, funções, classes ou variáveis definidas em outros arquivos do seu projeto. Isso significa que ele não fornece sugestões apenas com base no arquivo atual em que você está trabalhando; ele também pode referenciar outros arquivos para oferecer autocompleções de código mais precisas e relevantes. Esse recurso é particularmente útil quando você está trabalhando em projetos grandes, onde o código está distribuído em vários arquivos. A capacidade do GitHub Copilot de referenciar outros arquivos permite que ele compreenda melhor o panorama geral do seu projeto, resultando em sugestões mais contextualizadas. Isso pode melhorar significativamente sua eficiência na escrita de código e a qualidade geral do seu código.

Seja você um desenvolvedor experiente buscando aprimorar sua eficiência na escrita de código ou um iniciante tentando melhorar suas habilidades de programação, este laboratório fornecerá insights valiosos sobre como o **GitHub Copilot** pode ser uma ferramenta poderosa em sua jornada. Ao final deste desafio, você pretende demonstrar à **Contoso Ltd.** como esses recursos avançados do **GitHub Copilot** podem melhorar significativamente a eficiência da escrita de código e a qualidade geral do código, reforçando ainda mais os benefícios da integração da IA no fluxo de desenvolvimento. Vamos começar!

## Pré-requisitos

Certifique-se de ter o seguinte no ambiente integrado fornecido pelo CloudLabs:

- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub account](https://github.com/)
- [GitHub Copilot extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) installed in VS Code.

## Objectivos do Desafio:

1. Crie uma nova pasta chamada **DemoApp** em **C:/Users/azureuser**.

2. **Utilize o GitHub Copilot Workspace no aplicativo de Banco de Dados de Contatos existente:**

   - Entenda e explore como o recurso Workspace funciona.

   - Forneça alguns prompts ao agente do workspace no seu ambiente VS Code e revise suas saídas, como perguntar sobre coisas relevantes relacionadas ao seu workspace atual, gerar novas funcionalidades, identificar problemas em qualquer arquivo e mais.

     >**Dica:** Use referências de arquivos **@workspace**, **@vscode** e **@terminal** para os prompts.

3. **Utilize o GitHub Copilot Workspace para criar um novo aplicativo React chamado Expense Tracker:**

   - Crie a estrutura fundamental do workspace do zero usando o recurso **GitHub Copilot Workspace** em `C:/Users/azureuser/DemoApp`.

     >**Dica:** Peça ao Copilot para criar um workspace para um novo aplicativo React Expense Tracker com todos os arquivos e código necessários.

   - Desenvolva os componentes individuais necessários no esboço do aplicativo Expense Tracker usando as capacidades transformadoras do **GitHub Copilot**.

     >**Dica:** Use a referência de arquivo **@workspace** para adicionar funcionalidades a todos os arquivos.

   - Debug todos os possíveis erros que surgirem ao executar o aplicativo Expense Tracker usando o GitHub Copilot Workspace.

   - Execute o aplicativo em seu sistema local com sucesso. O aplicativo deve ser semelhante ao exemplo abaixo:

      ![](../../media/app-working.png)

   <validation step="76e12adb-fdce-4aea-a013-b0f721a72995" />

   <validation step="2458065d-db29-4909-a6a8-6be48c96d04b" />

4. **Utilize as capacidades de file referencing:**

      - Entenda como o GitHub Copilot referencia arquivos em seus documentos e como isso ajuda no fluxo de código.

      - Forneça alguns prompts que exijam que o GitHub Copilot referencie múltiplos arquivos no seu projeto com vários arquivos e analise as referências corretamente, ou seja, forneça prompts que descrevam os usos do arquivo **index.js** no aplicativo **Expense Tracker** que você construiu anteriormente.

      - Forneça um prompt usando referências de arquivos que integre o campo **Date** no documento **ExpenseForm** do seu **Expense Tracker Application** e exiba-o no **ExpenseItem**, e então permita que você classifique as despesas por data no componente **ExpenseList**.

      - output deve ser semelhante ao exemplo abaixo:

         ![](../../media/app-working-date.png)

## Critério de Sucesso:

- Certifique-se de entender o funcionamento do GitHub Copilot Workspace e do Referenciamento de Arquivos.

- Certifique-se de que você forneceu os prompts relevantes para testar o funcionamento do agente do workspace e do referenciamento de arquivos.

- Verifique se o aplicativo de rastreamento de despesas está funcionando corretamente.

- Verifique os resultados gerados pelos seus prompts e sua precisão.

- Verifique se o componente de data foi adicionado ao seu aplicativo e está funcionando corretamente.

## Recursos Adicionais:

- Consulte [aqui](https://githubnext.com/projects/copilot-workspace/) para mais informações.

## Conclusão

Neste desafio, você adquiriu uma compreensão mais profunda de como funcionam o **Github Copilot Workspace and File Referencing** e como eles podem melhorar seu processo de escrita de código. Ao utilizar essas funcionalidades de forma eficaz, você pode melhorar significativamente a sua eficiência na escrita de código e a qualidade geral do seu código. Seja você um desenvolvedor experiente ou iniciante, esses insights certamente serão valiosos em sua jornada enquanto desenvolvedor.

### Clique em Avançar >> para prosseguir com o próximo desafio.

![](../../media/next-page-p.png)