# Madson Ferrari

Olá pessoal, eu sou Madson Ferrari, Engenheiro eletricista, pós graduado em Mecatrônica pela UFRJ e entusiasta pela área de informática, programação e Innovation

## Você pode me encontrar aqui:

[![Perfil DIO](https://img.shields.io/badge/-Meu%20Perfil%20na%20DIO-0077B5?style=for-the-badge&logo=gitbook&logoColor=white)](https://www.dio.me/users/madson_ferrari)

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-000?style=for-the-badge&logo=linkedin&logoColor=30A3DC)](https://www.linkedin.com/in/MadsonFerrari/)

[![Youtube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@MadsonFerrari)

# Análise de sentimentos com Language Studio


- A primeira etapa foi assitir ao módulo de Análise de texto do curso da DIO dentro do bootcamp AI-900


- Acessar o [Portal Azure](https://portal.azure.com) usando as credenciais

![Tela Inicial](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%20Inicial.PNG)

Depois temos que criar um recurso do Language na Guia AI + Machine Learning.

![Imagem Language](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%202%20Create%20resurce.PNG)

Escolher **Continue to create a resource**

![Imagem da criação de recurso](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%203%20-%20Criando%20recurso%20de%20language.PNG)

Aparecerá a tela de criação de recursos

![Tela de recursos](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%204.PNG))

Selecionei **+Create a resource**
- Procurar e selecionar **Azure AI Services** ,clicar em CREATE e colocar os seguintes ajustes:
    - **Subscription:** *Sua conta do Azure*
    - **Resource group:** *Nome do Recurse Group*
    - **Region:** *East US 2*
    - **Name:** *Nome desejado*
    - **Price Tear:** *Free F0* ou *Standard S0*
    - **Box de termos:** *Selecionada*

> [!NOTE]
> No **Price Tear** a opção Free F0 pode não aparecer se já tiver sido escolhida anteriormente 

- Selecione **Review + create** e então selecione **Create**.

![Imagem da criação](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/tela%205.PNG)  

Espere a criação do espaço de trabalho (levou alguns minutos) 

![Deploy](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%206%20-%20Deployed.PNG)

Depois de criado acessar o [portal do Language Cognitive] (https://language.cognitive.azure.com/home)

## Reconhecimento de Texto com Language Studio

Recurso criado e Deploy feito, basta escolher o recurso e classificação de texto no Language Studio.

![Language Studio Home](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%207%20-%20Language%20Cognitive.PNG)

> [!NOTE]
> **Esta parte pode demorar alguns minutos pois o recurso demora para aparecer na lista**
> Conforme imagem abaixo.

![imagem da tela de recursos](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%20de%20recurso.PNG) 

Para teste da detecção de Sentimento eu preparei um texto com várias sentenças sobre o opinião de um cliente em um restaurante.

[link do Arquivo de Texto](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/inputs/Senten%C3%A7as-2.txt)

Aqui temos um preview do texto.

![Texto escolhido](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Texto%20Escolhido.PNG)

Basta carregar o texto na opção **Browse for a file** e depois clicar em RUN e pronto. O Language Studio retorna a análise de sentimento do texto.

Aqui podemos verificar que ele detectou o sentimento negativo nesta parte do texto onde citei que a comida estava fria e com muito sal. Note que mesmo escrevendo a palavra Garçon errada ele conseguiu interpretar a frase e detectar meu sentimento de desgosto.

![Imagem](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%2010.PNG)

### A pontuação é importante

Submeti o mesmo texto varias vezes e alterei a pontuação da frase final para testar.

![Frase final](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%209.PNG)

![Frase final exclamativa](https://github.com/MadsonFerrari/Projeto_Language_Studio/blob/main/Prints%20de%20tela/Tela%2011.PNG)

## Considerações finais

### As ferramentas do Azure e language Studio demonstraram que são muito úteis em diversos projetos e que conseguem um acerto muito alto tanto na detecção de texto, fala para texto, texto para fala, Contexto e sentimentos. 


