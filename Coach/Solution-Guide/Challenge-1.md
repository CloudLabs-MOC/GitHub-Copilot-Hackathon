# Desafio 1: Primeiros passos com o GitHub Copilot - Guia da Solução

## Task 1: Configurar o GitHub Copilot no VS Code

Nesta tarefa, você instalará a extensão GitHub Copilot no VS Code.

1. Abra o Visual Studio Code a partir da tela inicial.
   
   ![Picture1](../../media/task1.1.png)

1. Clique no ícone de **Extensions (1)** na barra de atividades, no lado esquerdo da janela do Visual Studio Code.
   
1. Na caixa de pesquisa "**Search Extensions in Marketplace**", digite e procure pela extensão **GitHub Copilot (2)** extension.
   
1. Selecione  **GitHub Copilot (3)** na lista de resultados.

1. Clique no botão **Install (4)**.

   ![Picture1](../../media/task1.2.png)

## Task 2: Login com uma conta do GitHub

Nesta tarefa, você fará login na sua conta GitHub através da extensão GitHub Copilot.

1. Após a instalação, no canto inferior direito, clique no prompt **Sign in to GitHub**.
   
   ![Sign in to GitHub](../../media/signingit.png)
   
1. No popup, clique em **Allow**.

   ![Allow](../../media/allow.png)

1. Na página de login do GitHub, insira suas credenciais do GitHub e clique em **Sign in**.

1. Para verificar o login na sua conta GitHub, entre no Outlook na máquina virtual do laboratório em uma janela **Private**  (https://outlook.office365.com/mail/) usando suas credenciais do GitHub, localize o e-mail contendo o código de verificação e selecione **Verify**.

1. Clique em **Authorize Visual-Studio-Code** para fornecer permissões adicionais ao GitHub para o VS Code.

## Task 3: Utilizar GitHub Codespaces com Copilot

Nesta tarefa, você criará um novo codespace para o seu repositório GitHub e usará a extensão GitHub Codespaces para fazer commit e enviar alterações diretamente do VS Code para o repositório GitHub de sua escolha.

1. Bifurque o repositório **https://github.com/CloudLabsAI-Azure/Code-Generation-Refactoring** Na página inicial do seu repositório, clique na guia **Code** **(1)** localizada na canto superior esquerdo da tela. Clique no botão **Código** **(2)** localizado no meio da página.

1. Clique na tab **Codespaces (1)** na caixa que aparece e, em seguida, clique no botão **Create codespace on main (2)**.

   >**Nota**: Se um prompt pop-up não aparecer no browser para abrir o Visual Studio Code, inicie manualmente o Visual Studio Code a partir da área de trabalho e feche-o. Em seguida, volte para o browser, atualize a página e inicie o codespace que foi criado anteriormente.

   ![GitHub-Codespaces](../../media/github-codespaces.png)

1. Se o Codespace não abrir no seu Visual Studio Code, navegue até o seu repositório GitHub, clique em **Code**, clique no botão de reticências para o seu codespace atual e depois clique em **Open in Visual Studio Code**.

1. Você verá um pop-up. Clique em **Open** para continuar. Em seguida, outra janela pop-up aparecerá dentro do Visual Studio Code (VS Code), onde você deve selecionar novamente **Install and Open** para prosseguir.

   ![](../../media/open.png)

   ![](../../media/codespaces.png)

1. No canto inferior direito, você receberá um prompt para fazer login no GitHub.

1. Em seguida, quando o popup aparecer, clique em **Allow**.

   >**Nota**: Aguarde cerca de 2 minutos para o codespace se inicializar.

   ![](../../media/allow.png)

1. Clique em **Authorize Visual-Studio-Code** quando a tab Authorize GitHub for VS Code aparecer no navegador.

1. Verifique se o seu codespace está em execução.

1. Agora você pode editar os arquivos do seu repositório GitHub, fazer commit e enviar as alterações diretamente para o GitHub através do VS Code.

## Task 4: Explorar as funcionalidades de GitHub Copilot

Nesta tarefa, você explorará vários recursos do GitHub Copilot por meio de um script Python simples que define uma função para calcular o fatorial de um número.

1. Abaixo está um script Python simples que define uma função para calcular o fatorial de um número. Vamos usá-lo para explorar os recursos do GitHub Copilot.

   ```
   def factorial(n):
       if n == 0:
           return 1
       else:
           return n * factorial(n-1)

   choice = int(input("Enter a number to calculate its factorial: "))
   print(f"The factorial of {choice} is {factorial(choice)}")
   ```

1. Selecione todo o código, clique com o botão direito e veja as funcionalidades do **Copilot**.

   ![](../../media/CopilotFeatures.png)

1. O recurso **Start in Editor (1)** permite que você faça perguntas ou forneça feedback diretamente no seu editor de código enquanto usa o GitHub Copilot.

1. O recurso **Explain This (2)** fornece uma explicação detalhada de como o código funciona e sua funcionalidade.

   ![](../../media/copilot-features-explain.png)

1. O recurso **Fix This (3)** propõe uma solução para os problemas no código selecionado.

   ![](../../media/copilot-features-fix.png)

1. O recurso **Generate Docs (4)** gera documentação ou comentários sobre o código selecionado.

   ![](../../media/copilot-features-docs.png)

1. O recurso **Generate Tests (5)** gera testes unitários para o código selecionado. Neste caso, o GitHub Copilot gera um script de teste em Python, que você pode executar para visualizar os resultados.

   ![](../../media/copilot-features-tests.png)

   ![](../../media/copilot-features-tests-cmd.png)

1. Você também pode perguntar como fazer algo no terminal, perguntar sobre o VS Code ou sobre o seu workspace simplesmente digitando o caractere especial **@** na janela do GitHub Copilot Chat.

   ![](../../media/copilot-features-chat.png)

1. O GitHub Copilot também ajuda a criar o esqueleto do código para um novo workspace, a gerar um novo notebook Jupyter, e vários tipos de documentação, como Markdown e Javadoc.

## Task 5: Geração de Código com Copilot e Copilot Chat

Nesta tarefa, você irá criar código em Python/JS para construir uma calculadora e usará a API Key do OpenWeatherMap para obter dados meteorológicos das APIs de clima.

1. Abra a janela de chat do GitHub Copilot e peça ao GitHub Copilot para criar código em Python/JS para construir uma calculadora usando o prompt abaixo.

   ```
   Create a Python/JS based code to build a calculator 
   ```

   ![](../../media/copilot-calculator.png)

1. Observe como o GitHub Copilot cria código para construir uma calculadora nas linguagens Python e JS. Salve os arquivos para executar os testes.

   - Python code to build a calculator:
     ```
     def add(x, y):
     return x + y

     def subtract(x, y):
     return x - y

     def multiply(x, y):
     return x * y

     def divide(x, y):
     if y == 0:
        return "Error! Division by zero."
     else:
        return x / y

     print("Select operation:")
     print("1.Add")
     print("2.Subtract")
     print("3.Multiply")
     print("4.Divide")

     while True:
        choice = input("Enter choice(1/2/3/4): ")

        if choice in ('1', '2', '3', '4'):
          num1 = float(input("Enter first number: "))
          num2 = float(input("Enter second number: "))

     if choice == '1':
            print(num1, "+", num2, "=", add(num1, num2))

     elif choice == '2':
            print(num1, "-", num2, "=", subtract(num1, num2))

     elif choice == '3':
            print(num1, "*", num2, "=", multiply(num1, num2))

     elif choice == '4':
            print(num1, "/", num2, "=", divide(num1, num2))
     break

     else:

     print("Invalid Input")

     ```

   - JS code to build a calculator
     ```
      // Function to add two numbers
      function add(a, b) {
        return a + b;
      }

      // Function to subtract two numbers
      function subtract(a, b) {
        return a - b;
      }

      // Function to multiply two numbers
      function multiply(a, b) {
        return a * b;
      }

      // Function to divide two numbers
      function divide(a, b) {
        if (b === 0) {
          return "Error: Division by zero";
        }
        return a / b;
      }

      // Declare and assign values to num1 and num2
      var num1 = 5;
      var num2 = 3;

      console.log("Addition:", add(num1, num2));
      console.log("Subtraction:", subtract(num1, num2));
      console.log("Multiplication:", multiply(num1, num2));
      console.log("Division:", divide(num1, num2));
     ```
   > **Nota:** Declare as duas variáveis/números antes de executar os testes através do JS.

1. Execute os testes para os arquivos experimentando com diferentes operações para verificar o funcionamento da calculadora.

1. Para obter os dados meteorológicos das APIs de clima, primeiro faça login no site da OpenWeatherMap API (https://openweathermap.org/). Na dropdown do seu perfil de usuário no canto superior direito, clique em **My API keys**. Você pode usar a chave de API padrão ou criar uma nova para obter os dados meteorológicos usando o código.

   ![](../../media/weather-api-keys.png)

1. Abra a janela de chat do GitHub Copilot e peça ao GitHub Copilot para criar um aplicativo baseado em Python/JS para obter dados meteorológicos das APIs de clima.

   ```
   Create a Python/JS based app to get weather data from weather APIs
   ```

   ![](../../media/copilot-weather-api.png)

1. Observe como o GitHub Copilot cria código para obter dados meteorológicos das APIs de clima nas linguagens Python e JS.

   - Python:
     ```
     import requests

     def get_weather(city):
       API_KEY = 'ENTER YOUR WEATHER API KEY HERE'
       BASE_URL = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY}"
       response = requests.get(BASE_URL)
       data = response.json()
       main = data['main']
       print(f"Temperature: {main['temp']}")
       print(f"Humidity: {main['humidity']}")
       print(f"Weather: {data['weather'][0]['description']}")

     city = input("Enter the city: ")
     get_weather(city)
     ```
   - JS:
     ```
     async function getWeather(city) {
        const API_KEY = 'ENTER YOUR WEATHER API KEY HERE';
        const BASE_URL = `http://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${API_KEY}`;
        const response = await fetch(BASE_URL);
        const data = await response.json();
        console.log(`Temperature: ${data.main.temp}`);
        console.log(`Humidity: ${data.main.humidity}`);
        console.log(`Weather: ${data.weather[0].description}`);
     }

     const city = 'Mumbai';  // Replace with the city you want to get the weather for
     getWeather(city);
     ```
   > **Nota:** Digite o nome da cidade antes de executar os testes através do JS.

1. Execute os testes para os arquivos inserindo diferentes cidades para verificar se os dados meteorológicos estão sendo obtidos das APIs de clima.

1. Envie os arquivos para seu repositório GitHub bifurcado **CloudLabsAI-Azure/Code-Generation-Refactoring**.

## Task 6: Refactoring & Debugging de Código

Nesta tarefa, você estará refatorando e efetuando debug de código Python mal escritos usando o GitHub Copilot e testando alguns cenários.

1. Copie o código abaixo para um novo arquivo no VS Code.

   ```
   #A poorly written example of a program in Python. It prompts the user for the number of elements to sum, takes those integers as input, and handles some basic error cases
      
   MAX = 100

   def calculate_sum(arr):
         result = 0
         for num in arr:
            result += num
         return result

   def main():
         try:
            n = int(input("Enter the number of elements (1-100): "))
            if not 1 <= n <= MAX:
                  print("Invalid input. Please provide a digit ranging from 1 to 100.")
                  exit(1)

            arr = []

            print(f"Enter {n} integers:")
            for _ in range(n):
                  try:
                     arr.append(int(input()))
                  except ValueError:
                     print("Invalid input. Please enter valid integers.")
                     exit(1)

            total = calculate_sum(arr)

            print("Sum of the numbers:", total)

         except KeyboardInterrupt:
            print("\nProgram terminated by user.")
            exit(1)

   if __name__ == "__main__":
         main()
   ```
1. Selecione todo o código, clique com o botão direito e clique em **Refactor using Copilot**, e peça ao Copilot para refatorar o código selecionado.

1. Você notará que o GitHub Copilot refatorou e corrigiu o código.

   ```
   #A poorly written example of a program in Python. It prompts the user for the number of elements to sum, takes those integers as input, and handles some basic error cases

   MAX = 100

   def calculate_sum(arr):
      return sum(arr)

   def main():
      try:
         n = int(input("Enter the number of elements (1-100): "))
         if not 1 <= n <= MAX:
            print("Invalid input. Please provide a digit ranging from 1 to 100.")
            exit(1)

         arr = []

         print(f"Enter {n} integers:")
         for _ in range(n):
            try:
               arr.append(int(input()))
            except ValueError:
               print("Invalid input. Please enter valid integers.")
               exit(1)

         total = calculate_sum(arr)

         print("Sum of the numbers:", total)

      except KeyboardInterrupt:
         print("\nProgram terminated by user.")
         exit(1)

   if __name__ == "__main__":
      main()
   ```

1. SSalve o arquivo e execute alguns casos de teste para verificar se o código refatorado pelo GitHub Copilot está correto.

1. Copie o código abaixo para um novo arquivo no VS Code.

   ```
   # Intentionally flawed Python program

   # importing modules
   import itertools, random

   # make a deck of cards
   deck = list(itertools.product(range(1,14),['Spade','Heart','Diamond','Club'])

   # shuffle the cards
   random.shuffle(deck)

   # draw five cards
   print("You got:")
   for i in range(5)
      print(deck[i][0], "of", deck[i][1]
   ```

1. Selecione todo o código, clique com o botão direito e selecione **Copilot**, e depois clique em **Fix This** para fazer debug do código selecionado

1. Você notará que o GitHub Copilot fex debug e corrigiu o código.

   ```
   # Intentionally flawed Python program

   # importing modules
   import itertools
   import random

   # make a deck of cards
   deck = list(itertools.product(range(1, 14), ['Spade', 'Heart', 'Diamond', 'Club']))

   # shuffle the cards
   random.shuffle(deck)

   # draw five cards
   print("You got:")
   for i in range(5):
      print(deck[i][0], "of", deck[i][1])
   ```

1. Salve o arquivo e execute alguns casos de teste para verificar se o código em que o GitHub Copilot efetuou debug está funcionando conforme o esperado.

### Clique em Avançar >> para prosseguir com o próximo desafio.

![](../../media/next-page-p.png)