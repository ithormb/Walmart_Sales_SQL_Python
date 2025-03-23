# Projeto End-to-End - Walmart Sales - ETL + BI + Machine Learning

![image](https://github.com/user-attachments/assets/7e1c055c-d639-4084-b984-7033194fba22)

## Contexto
O Projeto end-to-end consiste em utilizar o banco de dados de vendas por filiais da Walmart e gerar insights para a diretoria da empresa trabalhando em 2 frentes:
- Análise de Dados: Realizando o processo de ETL por meio de SQL e Python criou-se uma dashboard de performance de Vendas que apresentam indicadores, análises e insights importantes para a diretoria corporativa da empresa.   
- Machine Learning: Por meio da técnica de clusterização K-Means, realizando a categorização das filiais, facilitando análises gerenciais de forma clusterizada;

## Softwares e Linguagens Utilizadas
- **Softwares** - Microsoft Power BI (BI) e Visual Studio Code (VS Code);
- **Linguagens** - SQL e Python;

## Biblioteca Utilizada
- **Manipulação e Análise dos dados** - Pandas
- **Construção dos gráficos** -
- **Modelos de Machine Learning** -

## Parte 1 - Integração API Kaggle

A integração com a API Kaggle facilita o processo de extração do banco de dados. Assim, seguindo os passos abaixo você consegue conectar a API no VS Code:

1. Obtenha o token do Kaggle API selecionando em **Configuração -> API** no seu perfil do Kaggle e selecione **"Create New Token"**. Assim, você irá realizar o download do arquivo JSON.
2. Salve o arquivo `kaggle.json` no seu usuário local em uma pasta com o nome `.kaggle`.
3. Instale a biblioteca da API Kaggle no VS Code e autentique-se:

```python
!pip install -q kaggle
import kaggle
from kaggle.api.kaggle_api_extended import KaggleApi

api = KaggleApi()
api.authenticate()

api.dataset_download_file('najir0123/walmart-10k-sales-datasets',
                          file_name='Walmart.csv')

```

## Parte 2 - ETL e Bussiness Problems

Nessa etapa utiliza-se o VS Code como software para realizar todo o processo de *Extract, Transformation and Load* (ETL) dos dados, além da resolução dos *business problems* levantados que irão auxiliar no melhor entendimento do *dataset*. O arquivo colocar_o_nome_do_arquivo.ipynb dessa etapa está em anexo acima. Abaixo, seguem os *business problems* mapeados:

1. Qual os diferentes métodos de pagamento, número de transações e quantidades vendidas por método de pagamento;
2. Qual a maior "rated" por categoria em cada filial? Mostre a filial, categoria e sua média de "rating";
3. Qual o melhor dia e mês de venda para cada filial, baseado no número de transações;
4. Qual o total de itens vendidos por método de pagamento?
5. Determine a média, mínimo e máximo "rating" dos produtos por cada cidade;
6. Determine a média da margem de lucro (profit margin) de cada cidade;
7. Qual é o método de pagamento mais comum para cada filial;
8. Qual o total de vendas de cada filial por período do dia (Manhã, Tarde e Noite) 
9. Identifique os 5 maiores decaimento de receita por filial dos anos de 2022 para 2023;
10. Qual a receita por mês para cada ano?

A partir dos questionamento foi possível realizar algumas análises iniciais que facilitaram o entendimento detalhado do banco de dados e dos painéis necessários pela corpo gerencial da empresa. Assim, na próxima etapa foi realizado o processo de construção da dashboard de acompanhamento de vendas e geração de insights.

## Parte 3 - Power BI de Performance de Vendas

Para a construção do dashboard de **Performance de Vendas**, foi utilizado o software **Power BI**, seguindo um processo dividido em **quatro etapas macro**. Esse fluxo garante um painel de qualidade e alinhado com as expectativas dos usuários.

#### Etapa 1 - Definição da Finalidade e Objetivo do BI  
Nesta etapa, é fundamental entender **qual problema de negócio o dashboard irá resolver** e quem são os usuários finais da análise. Assim, foram definidos os seguintes pontos:  
- O BI tem o objetivo de realizar o acompanhamento da performance de vendas e geração de ingishts para os gerentes da empresa;
- É necessário parametrizar as informações em 3 macro indicadores: Margem de Lucro, Faturamento e Quantidades Vendidas;
- A partir da parametrização acima, o objetivo do painél trazer o acompanhamento de vendas por série cronologócia, Filiais, categoria de produtos, entre outras variáveis; 

Esse entendimento permite estruturar um dashboard que seja realmente útil e direcionado para a tomada de decisões.

#### Etapa 2 - Definição das Métricas e Indicadores
Com os objetivos definidos, o próximo passo é **selecionar os KPIs (Key Performance Indicators)** que serão monitorados no painel.Assim, foram definidos os 3 KPIs principais que nortearão as métricas e gráficos e tabelas do painel.

- **Faturamento** - Valor gerado de receita do total dos produtos vendidos;
- **Margem de Lucro** - Quanto de lucro pelas vendas realizadas;
- **Quantidade de vendas** - Número de vendas realizadas;

Posteriormente foram analisados e definidos os gráficos e tabelas que iriam compor o painel, de acordo com as informações mais importante e necessárias pelo o time gerencial. A definição de métricas bem estruturadas evita dashboards confusos e garante que os dados sejam relevantes para a empresa.

#### Etapa 3 - Extração e Tratamento dos Dados  
Nesta fase, os dados extraídos passam por um processo de limpeza e transformação para garantir sua qualidade e integridade. As principais atividades incluem:  
- **Remoção de valores nulos e duplicados**;  
- **Tratamento de outliers** para evitar distorções nas análises. Nesse contexto, foram eliminados os dados de vendas de 2012 que não apresentavam dados do ano inteiro (dados apenas de Jan/12 até Mar/12);
- **Criação de colunas calculadas e métricas no Power Query**;  
- **Relacionamento entre tabelas no modelo de dados** para garantir a correta conexão entre fontes de informação.  

#### Etapa 4 - Criação do Layout  
A última etapa envolve o design e a construção do dashboard. Aqui, considera-se:  
- **Disposição dos gráficos e tabelas** para facilitar a interpretação;  
- **Uso de cores e estilos visuais** alinhados com a identidade da empresa;  
- **Interatividade** com filtros e segmentações que permitam diferentes visões dos dados;  
- **Testes de usabilidade** para garantir que os usuários entendam o painel e possam extrair insights rapidamente.  

Assim, finaliza-se a construção do dashboard de gestão da performance de vendas, no qual o arquivo `walmartesalesBI.pbix` está disponível para download.

## Parte 4 - Machine Learning


## Parte 5 - Apendizados dos modelos de ML


