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

Não! O Document Intelligence não é apenas um OCR. Ele é baseado em IA e não apenas reconhece o texto mas também ele interpreta o conteúdo identificando as informações para você.
Tudo isto baseado em treinamento com vários documentos. Ou seja, ele é capaz de reconhecer palavras chaves e informações como:

- Campo Nome e o valor do nome
- Campo Endereço e qual é o valor do mesmo
- Campo Empresa e o nome do estabelecimento
- Campo do Produto e descrição do mesmo
- Campo do Valor
- Campo de quantidade e valor
- etc...

Desta forma suas informações podem ser catalogadas em tabelas que você pode armazenar no próprio Storage do Azure.
Esta capacidade de reconhecer e extrair texto, layout e palavras chaves é conhecido como *Document Analysis* ou Análise de Documentos em Português.

Mas você deve estar pensando: Os campos estão em Inglês e as minhas notas que recebi estarão em Português, e agora?

Bem, o treinamento da plataforma é bem completo e reconhece a maioria dos idiomas mas, se você tiver problemas com os Prebuilt models
que são os modelos pré treinados, você pode criar modelos Customizados ou *Custom Models* para treinar de acordo com a sua necessidade.
Não é demais? 

# Vamos ver passo a passo como fazer:  

A primeira etapa é logar do [Document Intelligence Studio](https://formrecognizer.appliedai.azure.com/studio) e logar na sua conta da Microsoft

Depois clicamos na Engrenagem e escolhemos criar um recurso

![Imagem](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0_1.PNG)

Selecione *Resource*, Clique na sua *Subscription* e clique *Create a new resource* 

![Imagem2](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0_2.PNG)

Vai aparecer a tela de criação de recurso

![Imagem3](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0_3.PNG)

Escolha:

   - **Subscription:** *Sua conta do Azure*
   - **Resource group:** *Nome do Recurse Group* eu escolhi DOC_TEST3
   - **Region:** *East US 2*
   - **Name:** *Nome desejado* Eu escolhi TEST2
   - **Price Tear:** *Free F0* ou *Standard S0*
   - **Box de termos:** *Selecionada*

> [!NOTE]
> No **Price Tear** a opção Free F0 pode não aparecer se já tiver sido escolhida anteriormente 

Selecione **CONTINUE** e revise as escolhas mostradas

e então clique **Finish** para concluir.

![Imagem4](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0_4.PNG)

Pode ocorrer um erro se você já tiver usado a *Free F0* anteriormente

![Imagem5](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0_5.PNG)

Neste caso cique em *Back* para voltar e escolha a Opção *Standard S0*

![Imagem6](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0_6.PNG)
 
Revise novamente e Click *Finish* para concluir e criar o recurso

![Imagem7](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0_7.PNG)  

Espere a criação do espaço de trabalho (leva aproximadamente 1 minuto)

Pronto seu recurso está criado e aparecerá na tela.

![Imagem8](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela0_8.PNG)  

mantenha esta janela aberta e vamos para próxima parte

## Reconhecimento de um recibo usando o *Document Intelligence* 

![Imagem9](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Telas/Tela3.PNG)  

Para este exemplo podemos baixar um [recibo](https://aka.ms/mslearn-receipt) 

Vamos usar também outros recibos, agora em português como [este](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Recibo/Recibo_2.jpg) 

![Recibo](https://github.com/MadsonFerrari/Projeto_Cognitive_Search/blob/main/Recibo/Recibo_2.jpg)







## Considerações finais

### As ferramentas do Azure e language Studio demonstraram que são muito úteis em diversos projetos e que conseguem um acerto muito alto tanto na detecção de texto, fala para texto, texto para fala, Contexto e sentimentos. 


