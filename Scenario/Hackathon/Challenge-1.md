# Desafio 1: Primeiros passos com o GitHub Copilot

### Tempo Estimado: 45 Minutos

## Introdução

Como desenvolvedor de software na **Contoso Ltd.**, uma empresa líder em desenvolvimento de software, você é encarregado de pesquisar e implementar ferramentas e tecnologias inovadoras para melhorar o processo de desenvolvimento e a produtividade da empresa. A empresa está especialmente interessada em soluções que possam melhorar a eficiência do código, otimizar o processo de desenvolvimento e aprimorar a colaboração entre suas equipes distribuídas globalmente.

A **Contoso Ltd.** identificou o  **GitHub Copilot**, um assistente de desenvolvimento com IA, como uma solução em potencial e inscreveu você em uma série de desafios para explorar e entender suas capacidades. Sua missão é começar a utilizar o  **GitHub Copilot**, configurá-lo em seu ambiente de desenvolvimento, explorar seus recursos e usá-lo para geração de código e sugestões. O **GitHub Copilot** é um companheiro de desenvolvimento inovador, alimentado por IA e integrado perfeitamente no Visual Studio Code, projetado para aprimorar sua experiência de desenvolvimento. Aproveitando os modelos de Machine Learning, o Copilot auxilia os desenvolvedores na criação de código, sugerindo inteligentemente conclusões e gerando trechos de código contextualmente relevantes.

Imagine navegar em um projeto de desenvolvimento complexo e encontrar desafios que exigem atenção meticulosa aos detalhes. O **GitHub Copilot** entra em cena como seu aliado na programação, oferecendo sugestões perspicazes e autocompletação adaptada ao contexto do código. Isso não apenas aumenta a eficiência do desenvolvimento, mas também serve como uma ferramenta valiosa de aprendizado, proporcionando um entendimento mais profundo das estruturas e padrões de programação.

Você irá experimentar o **GitHub Copilot** em vários cenários de desenvolvimento, como a criação de uma calculadora baseada em Python/JavaScript e um aplicativo que busca dados meteorológicos de APIs. Também utilizará o GitHub Copilot para refatorar trechos de código fornecidos e depurar código intencionalmente defeituoso, entendendo assim o processo de melhoria de código e depuração eficaz. Além disso, você explorará a integração do **GitHub Copilot** com o GitHub Codespaces, um recurso que amplia o potencial colaborativo do seu ambiente de desenvolvimento. Isso permitirá que você entenda como o Copilot pode ser utilizado em um ambiente de desenvolvimento colaborativo, permitindo que equipes trabalhem em projetos de forma integrada, independentemente das fronteiras geográficas.

In this challenge series, you'll dive into **GitHub Copilot's** capabilities, starting with the setup and exploration of its features. From collaborative coding with GitHub Codespaces to experimenting with Copilot's suggestions and creating code for various tasks, you'll embark on a journey to harness the full potential of this revolutionary coding assistant. By the end of this challenge, you aim to demonstrate how **GitHub Copilot** can be effectively used to enhance coding productivity, improve code quality, and streamline the software development process at **Contoso Ltd**.

Nesta série de desafios, você explorará as capacidades do **GitHub Copilot**, começando pela configuração e exploração de seus recursos. Desde o desenvolvimento colaborativo com o GitHub Codespaces até a experimentação das sugestões do Copilot e a criação de código para diversas tarefas, você embarcará em uma jornada para aproveitar todo o potencial deste assistente de desenvolvimento revolucionário. Ao final deste desafio, você terá como objetivo demonstrar como o **GitHub Copilot** pode ser utilizado de forma eficaz para aumentar a produtividade na desenvolvimento, melhorar a qualidade do código e otimizar o processo de desenvolvimento de software na **Contoso Ltd**.

## Pré-requisitos

Certifique-se de ter o seguinte no ambiente integrado fornecido pelo CloudLabs:

> **Observação**: Os pré-requisitos já estão configurados no ambiente fornecido pelo CloudLabs. Se você estiver usando seu computador pessoal ou laptop, certifique-se de que todos os pré-requisitos necessários estejam instalados para completar este hackathon.

- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub account](https://github.com/)
- Módulos Python e NodeJs estão instalados em seu Lab-VM no diretório **C:\Program Files**.

## Login no GitHub

1. No desktop do LABVM, procure por **Microsoft Edge** **(1)**, clique no browser **Microsoft Edge** **(2)**.

   ![](../../media/Edge.png)

1. Navegue até a página de login do GitHub usando o URL fornecido abaixo:

   ```
   https://github.com/login
   ```

1. Na aba **Sign in to GitHub**, você verá a tela de login. Nessa tela, insira o seguinte email **email** **(1)** e a password **password** **(2)**. Em seguida, clique em **Sign in** **(3)**.

   >**Nota**:Para obter as credenciais do GitHub, navegue até a aba **Environment Details** e clique na opção **GitHub Credentials** para visualizar os pares de chave-valor do **GitHub UserEmail**, w **GitHub Password**. Você pode usar os botões de copiar na coluna de ações para ter os valores copiados instantaneamente. Alternativamente, é sugerido copiar os valores para um bloco de notas para fácil acessibilidade.

   ![](../../media/github-login.png)

1. Em seguida, para obter o código de autenticação, faça login no Outlook (https://outlook.office365.com/mail/) com as credenciais do GitHub fornecidas na aba Environment da etapa anterior. Após fazer login no Outlook, encontre o email recente contendo o código de verificação. Insira o código de verificação e clique em **Verify**.

   >**Observação:** O email contendo o código de verificação pode, às vezes, ir parar nas pastas de arquivamento/spam do seu Outlook.

   ![](../../media/authgit.png)

## Objectivos do Desafio:

1. **Configurar o GitHub Copilot no VS Code:**
      - Instalar a extensão do GitHub Copilot a partir do VS Code Marketplace.
      - Configurar a extensão de acordo com a suas preferências.

   <validation step="afc73673-26ad-4c49-b013-4632e09d8634" />

2. **Login com uma conta do GitHub:**
      - Faça login no GitHub dentro do Visual Studio Code usando as credenciais do GitHub fornecidas. Você pode encontrar essas credenciais em **Environment > GitHub Credentials**.
      - Na página de login do GitHub, insira suas credenciais do GitHub e clique em **Sign in**.
      - Para verificar o login da sua conta do GitHub, faça login no **Outlook** no Lab VM através de uma janela Privada (https://outlook.office365.com/mail/) usando suas credenciais do GitHub. Localize o email contendo o código de verificação e selecione **Verify**.
      - Clique em Authorize Visual Studio Code para fornecer permissões adicionais ao GitHub para o VS Code.

3. **Utilizar GitHub Codespaces com Copilot:**
      - Crie um Codespace para o seu repositório GitHub.
        >**Nota:** Navegue al repositorio **https://github.com/CloudLabsAI-Azure/Code-Generation-Refactoring** y bifurque (haga fork) este repositorio en la cuenta de GitHub proporcionada por CloudLabs para crear un nuevo Codespace.
      - Clone o repositório bifurcado acima no Visual Studio Code usando a conta GitHub fornecida pelo CloudLabs.
      - Entenda como o Copilot pode ser utilizado em um ambiente de codificação colaborativo.
      - Use o GitHub Codespaces para fazer push/commit dos arquivos locais do VS Code para o GitHub nos próximos desafios.

4. **Explorar as funcionalidades de GitHub Copilot:**
      - Experimente o Copilot em vários cenários de programação.
      - Use as sugestões do Copilot para acelerar seu processo de escrita de código.

        >**Dica:** Acesse a janela de Sugestões do GitHub Copilot usando o atalho **Ctrl+Enter** no seu VS Code.

5. **Geração de Código com Copilot e Copilot Chat:**
      - Crie código baseado em Python/JS para construir uma calculadora.
         - Utilize o GitHub Copilot para gerar código em Python ou JavaScript que cria uma calculadora básica.
         - Depois de escrever o código, salve o arquivo como calculator.py se estiver usando Python, ou calculator.js se estiver usando JavaScript, e envie-o para seu repositório GitHub bifurcado **CloudLabsAI-Azure/Code-Generation-Refactoring**.
         - Experimente diferentes operações matemáticas e interações com o usuário.
      - Crie um aplicativo baseado em Python/JS para obter dados meteorológicos das APIs do OpenWeatherMap.
         - Inscreva-se no site do OpenWeatherMap (https://openweathermap.org/).
         - Utilize o Copilot para gerar código Python/JS que interage com as APIs de clima para recuperar dados meteorológicos.
         - Salve este arquivo como weather_script.py para Python ou weather_script.js para JavaScript e envie-o para seu repositório GitHub bifurcado do CloudLabsAI-Azure/Code-Generation-Refactoring.

   <validation step="b5244888-2b42-4686-b326-465182a86561" />

6. **Refactoring & Debugging de Código:**

      - Refatore o código `sum_elements.py` do seu repositório GitHub bifurcado **CloudLabsAI-Azure/Code-Generation-Refactoring** usando o Copilot, entendendo o processo de melhoria do código.

        >**Sugerencia:** Utilice la función Refactor de GitHub Copilot.

      - Depure o código `card_draw.py` de maneira eficaz a partir de seu repositório GitHub bifurcado **CloudLabsAI-Azure/Code-Generation-Refactoring** com a ajuda do Copilot, abordando e corrigindo problemas identificados.

         >**Sugerencia:** Utilice la función Corregir de GitHub Copilot.

## Critério de Sucesso:

- Verifique se o GitHub Copilot está instalado e configurado corretamente no Visual Studio Code e se você está logado.
- Explore com sucesso a integração do GitHub Codespaces e compreenda seus recursos de colaboração.
- Experimente o Copilot em cenários de desenvolvimento, verificando suas capacidades de geração de código.
- Verifique se o código em Python/JS para uma calculadora e um aplicativo para obter dados meteorológicos usando o Copilot foram criados e executados com sucesso.
- Verifique se o código escolhido foi refatorado com sucesso, com melhoria na legibilidade e qualidade geral.
- Verifique se um trecho de código com erros intencionais foi corrigido com sucesso usando as sugestões do Copilot.

## Recursos Adicionais:

- [Documentação do GitHub Copilot](https://github.com/github/copilot-docs)
- [Documentação do GitHub Codespaces](https://docs.github.com/en/codespaces)

### Conclusão

Neste desafio, você configurou com sucesso o GitHub Copilot no Visual Studio Code, ajustou as configurações da extensão e fez login com sua conta do GitHub. Você também foi bem-sucedido na criação de código em Python/JS para uma calculadora e um aplicativo para buscar dados meteorológicos das APIs do OpenWeatherMap. Além disso, você melhorou suas habilidades de escrita de código ao refatorar trechos de código e depurar com a assistência do Copilot.

### Clique em Avançar >> para prosseguir com o próximo desafio.

![](../../media/next-page-p.png)