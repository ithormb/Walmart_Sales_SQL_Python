# Projeto End-to-End - Walmart Sales - ETL & BI & Machine Learning

![image](https://github.com/user-attachments/assets/7e1c055c-d639-4084-b984-7033194fba22)



## Contexto
O Projeto end-to-end consiste em utilizar o banco de dados de vendas por filiais da Walmart e gerar insights para a diretoria da empresa trabalhando em 2 frentes:
- Análise de Dados: Realizando o processo de ETL por meio de SQL e Python criou-se uma dashboard de performance de Vendas que apresentam indicadores, análises e insights importantes para a diretoria corporativa da empresa.   
- Machine Learning: Por meio da técnica de clusterização K-Means, realizando a categorização das filiais, facilitando análises gerenciais de forma clusterizada;

## Softwares e Linguagens Utilizadas
- **Softwares** - Microsoft Power BI (BI) e Visual Studio Code (VS Code);
- **Linguagens** - SQL e Python;

## Parte 1 - Integração API Kaggle
A integração com a API Kaggle facilita o processo de extração do banco de dados. Assim, seguindo os passos abaixo você consegue conectar a API no VS Code:
- Obtenha o token do Kaggle API selecionando em Configuração -> API no seu perfil do Kaggle e selecione em "Create New Token". Assim, você irá realizar o download do arquivo JSON;
- Salve o arquivo kaggle.json no seu usuário local em uma pasta com o nome .kaggle;
- Instale a biblioteca da API Kaggle no VS Code:
  - "!pip install -q kaggle"
  - import kaggle
  - from kaggle.api.kaggle_api_extended import KaggleApi
  - api = KaggleApi()
  - api.authenticate()
  - api.dataset_download_file ('najir0123/walmart-10k-sales-datasets',
                            file_name= 'Walmart.csv')

## Parte 2 - ETL e Bussiness Problems

Nessa etapa utiliza-se o VS Code como software para realizar o processo de tratamento de dados e resolver 9 questões de negócios que auxiliam no entendimento melhor dos dados para as etapas futuras. O arquivo .ipynb dessa etapa está em anexo acima;

## Parte 3 - Power BI de Performance de Vendas



