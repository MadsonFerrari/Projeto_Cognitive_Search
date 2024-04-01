# Madson Ferrari

Olá pessoal, eu sou Madson Ferrari, Engenheiro eletricista, pós graduado em Mecatrônica pela UFRJ e entusiasta pela área de informática, programação e Innovation

## Você pode me encontrar aqui:

[![Perfil DIO](https://img.shields.io/badge/-Meu%20Perfil%20na%20DIO-0077B5?style=for-the-badge&logo=gitbook&logoColor=white)](https://www.dio.me/users/madson_ferrari)

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-000?style=for-the-badge&logo=linkedin&logoColor=30A3DC)](https://www.linkedin.com/in/MadsonFerrari/)

[![Youtube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@MadsonFerrari)

# Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados


- A primeira etapa foi assitir ao módulo de Inteligencia de Documentos e mineração do conhecimento da DIO dentro do bootcamp AI-900
- Após o curso, eu recomendo muito que você faça o treinamento do Document Intelligence do Azure
- [Azure training](https://learn.microsoft.com/en-us/training/paths/document-intelligence-knowledge-mining/)


- Acessar o [Portal Azure](https://portal.azure.com) usando as credenciais

![Tela Inicial](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0.PNG)

Este curso é uma adicional ao curso da DIO e mostra passo a passo como trabalhar com a inteligência de Documentos dentro do Azure 
no Document Intelligence.

Neste curso rápido, você vai aprender a criar um recurso e enviar um documento, neste caso uma nota de despesa para ser feito o OCR e categorização

![Exemplo de recibo](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Recibo/receipt.jpg)

# Mas afinal não era isto que um OCR faz? Não basta eu fazer um OCR com um aplicativo e pronto?

Não! O Document Intelligence não é apenas um OCR. Ele é baseado em IA e não apenas reconhece o texto mas também ele interpreta o conteúdo identificando as informações para você
Tudo isto basedao em treinamento com vários documentos. Ou seja, ele é capaz de reconhecer palavras chaves e informações como:

- Campo Nome e o valor do nome
- Campo Endereço e qual é o valor do mesmo
- Campo Empresa e o nome do estabelecimento
- Campo do Produto e descrição do mesmo
- Campo do Valor
- Campo de quantidade e valor
- etc...

Desta forma suas informações podem ser catalogadas em tabelas que você pode armazenar no próprio Storage do Azure.
Esta capacidade de reconhecer e extrair texto, layout e palavras chaves é conhecido como *Document Analysis* ou Análise de Documentos em Português.

Mas você deve estar pensando: Os campos estã em Inglês e minhas notas e recebi estarão em Português, e agora?

Bem, o treinamento da plataforma é bem completo e reconhece a maioria dos idiomas mas se você tiver problemas com os Prebuilt models
que são os modelo pré treinados, você pode criar modelos Customizados ou *Custom Models* para treinar de acordo com a sua necessidade.
Não é demais? 

# Vamos ver passo a passo como fazer:  


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


