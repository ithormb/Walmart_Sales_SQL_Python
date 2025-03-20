# Projeto End-to-End - Walmart Sales - ETL + BI + Machine Learning

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

Nessa etapa utiliza-se o VS Code como software para realizar todo o processo de *Extract, Transformation and Load* (ETL) dos dados, além da resolução dos *business problems* levantados que irão auxiliar no melhor entendimento do *dataset*. O arquivo colocar_o_nome_do_arquivo.ipynb dessa etapa está em anexo acima. Abaixo, seguem os *business problems* mapeados:

1. Find different payment methods, number of transactions, and quantity sold by payment method
2. Identify the highest-rated category in each branch. Display the branch, category, and average rating
3. Identify the busiest day and month for each branch based on the number of transactions
4. Calculate the total quantity of items sold per payment method
5. Determine the average, minimum and maximum rating of products for each city
6. Determine the average profit margin (%) with respect to each city
7. Determine the most common payment method for each branch
8. Categorize sales into 3 group Morning, Afternoon, Evening find out which of the shift and number of invoices
9. 
  a. Identify 5 branch with highest decrease ratio
  b. Revenue compare to last year (current year 2023 and lat year 2022)

## Parte 3 - Power BI de Performance de Vendas



## Parte 4 - Machine Learning



