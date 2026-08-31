# 📱 Análise de Engajamento — Social Media Graph Analytics

*Análise de engajamento, influência e relacionamentos em mídias sociais com Neo4j, Cypher e Python.*

![Neo4j](https://img.shields.io/badge/Neo4j-Graph%20Database-4581C3?logo=neo4j&logoColor=white)
![Cypher](https://img.shields.io/badge/Cypher-Graph%20Query-018BFF)
![Python](https://img.shields.io/badge/Python-Data%20Processing-3776AB?logo=python&logoColor=white)
![Graph Analytics](https://img.shields.io/badge/Graph-Analytics-2E8B57)
![Marketing Analytics](https://img.shields.io/badge/Marketing-Analytics-FF6F00)
![Social Media](https://img.shields.io/badge/Social%20Media-Analytics-C13584)
![DIO](https://img.shields.io/badge/DIO-Neo4j%20Bootcamp-5A0FC8)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

---

## 📌 Sobre o Projeto

O **Análise de Engajamento** é um projeto de **Social Media Analytics baseado em grafos**, desenvolvido para explorar relações entre usuários, conteúdos, hashtags, categorias, localizações e padrões de engajamento em um contexto de Instagram Lifestyle.

A solução utiliza **Python, Neo4j e Cypher** para transformar dados originalmente tabulares em uma rede de relacionamentos, permitindo investigar questões de Marketing que seriam menos naturais de representar apenas com tabelas tradicionais.

O projeto combina:

- preparação e tratamento de dados;
- modelagem orientada a grafos;
- construção de nós e relacionamentos;
- consultas analíticas em Cypher;
- análise de influência;
- análise de comunidades;
- recomendação baseada em conexões;
- identificação de oportunidades de mercado;
- interpretação dos resultados sob uma perspectiva de negócio.

---

## 🎯 Objetivo

Explorar como **Graph Analytics** pode apoiar problemas de Marketing e Social Media por meio da análise de relações entre entidades.

Entre as questões investigadas estão:

- Quem são os usuários mais relevantes em diferentes categorias?
- Quais hashtags aparecem relacionadas dentro da rede?
- Como o engajamento varia de acordo com localização?
- Quais usuários ou conteúdos apresentam maior similaridade?
- Existem categorias com potencial de oportunidade?
- Como a influência pode se propagar entre diferentes segmentos?

---

## 💼 Problema de Negócio

O cenário considera uma empresa de Social Media Analytics interessada em transformar dados de redes sociais em insights capazes de apoiar decisões relacionadas a:

- campanhas;
- creators e influenciadores;
- segmentação;
- conteúdo;
- comunidades;
- posicionamento de marca;
- oportunidades de mercado;
- recomendação.

O domínio analisado contempla categorias como:

- Moda
- Viagens
- Fitness
- Alimentação
- Beleza
- Lifestyle

---

## 🧠 Por que Grafos?

Mídias sociais são naturalmente estruturadas como redes.

Usuários se relacionam com outros usuários, publicam conteúdos, utilizam hashtags, pertencem a categorias e estão associados a localizações.

Uma representação simplificada:

```text
Usuário
   │
   ├── POSTS_IN_CATEGORY ──> Categoria
   │
   ├── USES_HASHTAG ──────> Hashtag
   │
   ├── BASED_IN ──────────> Localização
   │
   ├── CREATED_CONTENT ───> Post
   │
   └── FOLLOWS ───────────> Usuário

## 🕸️ Modelo do Grafo

O projeto trabalha com entidades como:

- User
- Influencer
- Post
- Category
- Hashtag
- Location

e relacionamentos como:

- POSTS_IN_CATEGORY
- USES_HASHTAG
- BASED_IN
- CREATED_CONTENT
- FEATURED_IN
- FOLLOWS
- INTERACTED_WITH
- TOP_INFLUENCER_IN

## 📄 Documentação complementar:

Modelo do Grafo

Representação visual
<img width="800" height="400" alt="Modelo de grafo do projeto" src="https://github.com/user-attachments/assets/6c6ff067-38b7-408c-9fac-c26482ab3187" />

## 🏗️ Pipeline Analítico

Dataset
   ↓
Python
   ↓
Inspeção e Tratamento
   ↓
Dataset Limpo
   ↓
Neo4j
   ↓
Modelagem do Grafo
   ↓
Criação de Nós e Relacionamentos
   ↓
Cypher
   ↓
Graph Analytics
   ↓
Insights de Marketing

## 🐍 Preparação dos Dados

O script Python realiza uma análise inicial do dataset, incluindo:

quantidade de registros;
identificação das colunas;
distribuição por categoria;
estatísticas de seguidores e engajamento;
identificação de valores ausentes;
remoção de registros sem campos essenciais;
geração de uma versão limpa do dataset.

Arquivo:

Scripts/preparacao-dataset.py

A saída esperada é:

instagram_clean.csv

## 🗄️ Carga no Neo4j

O script de carga estrutura o grafo no Neo4j e inclui:

criação de índices;
criação de usuários;
criação de categorias;
criação de localizações;
processamento de hashtags;
criação de posts;
criação de relacionamentos;
identificação de usuários classificados como influenciadores.

Arquivo:

Scripts/carga-neo4j.cypher

## ⚠️ Relações simuladas

Algumas relações do projeto são geradas por regras demonstrativas, pois o dataset utilizado não contém necessariamente todas as conexões sociais reais necessárias para uma rede completa.

Por exemplo:

relações FOLLOWS podem ser inferidas a partir de categorias em comum;
interações podem ser simuladas considerando a taxa de engajamento;
datas podem utilizar valores aproximados ou placeholders.

Esses relacionamentos servem para demonstrar modelagem e análise de grafos, e não devem ser interpretados como observações reais de comportamento individual dos usuários.

🔎 Análises Desenvolvidas

## 👑 1. Top Influenciadores por Categoria

Identifica usuários com maior relevância dentro das categorias analisadas considerando métricas como seguidores, taxa de engajamento e volume de posts.

Arquivo:

Queries/01-top-influenciadores.cypher

Possíveis aplicações:

seleção de creators;
planejamento de campanhas;
influencer marketing;
análise competitiva.

## #️⃣ 2. Comunidades de Hashtags

Investiga hashtags utilizadas por usuários em comum para identificar associações e possíveis agrupamentos temáticos.

Arquivo:

Queries/02-comunidades-hastags.cypher

Possíveis aplicações:

estratégia de conteúdo;
identificação de temas;
descoberta de comunidades;
análise de afinidade.

##📍 3. Engajamento por Localização

Compara usuários por localização utilizando métricas como:

quantidade de usuários;
média de seguidores;
média de engajamento;
perfis relevantes.

Arquivo:

Queries/03-engajamento-localização

Possíveis aplicações:

segmentação geográfica;
campanhas regionais;
estratégias de mídia;
identificação de mercados locais.

## 🎯 4. Recomendação de Conteúdo e Perfis

Explora similaridades entre usuários considerando:

categorias em comum;
hashtags em comum;
relevância do perfil.

Arquivo:

Queries/04-recomendacao-conteudo.cypher

Possíveis aplicações:

recommendation systems;
creator discovery;
descoberta de perfis semelhantes;
personalização.

##📈 5. Gap de Mercado

Procura categorias com menor quantidade de influenciadores, mas níveis interessantes de engajamento.

Arquivo:

Queries/05-gap-mercado.cypher

Possíveis aplicações:

identificação de nichos;
análise de oportunidades;
estratégia de conteúdo;
posicionamento de marca.

## 🕸️ 6. Caminhos de Influência

Analisa conexões entre usuários de diferentes categorias e estima como relações de influência podem conectar segmentos da rede.

Arquivo:

Queries/06-caminhos-influencia.cypher

Possíveis aplicações:

análise cross-category;
campanhas multissegmento;
identificação de pontes entre comunidades;
network analysis.

## 💡 Insights de Negócio

A modelagem permite explorar questões relacionadas a:

creators relevantes por segmento;
concentração de influência;
comportamento de hashtags;
diferenças geográficas de engajamento;
afinidade entre usuários;
oportunidades em categorias menos exploradas;
conexões entre comunidades;
potencial de recomendação.

O objetivo não é apenas executar consultas em Cypher, mas transformar os resultados em informações úteis para decisões de Marketing.

🧹 Problemas e Desafios Documentados

Além das análises, o projeto registra situações encontradas durante preparação, modelagem e execução.

Encoding

Tratamento de problemas relacionados a caracteres especiais.

Problemas/01-encoding-caracteres.cypher

Hashtags

Tratamento de registros vazios ou mal formatados.

Problemas/02-hastags-invalidas.cypher

Performance

Considerações relacionadas à quantidade de relacionamentos e impacto na execução das consultas.

Problemas/03-performance-follow.cypher

Memória

Tratamento de limitações relacionadas ao processamento de grafos maiores.

Problemas/04-memoria-grafos-grandes.bash

Esses registros ajudam a demonstrar que projetos de dados envolvem não apenas modelagem, mas também qualidade, performance e limitações de infraestrutura.

🖥️ Evidências Analíticas

Consultas utilizadas para reproduzir algumas visualizações e resultados do projeto estão organizadas em:

Evidencias/

Arquivos:

01-visao-geral-rede.cypher
02-cluster-moda.cypher
03-top-influenciadores-tabela.cypher

##🎨 Visualização

O repositório também mantém uma configuração de estilo utilizada como apoio à visualização do grafo:

Assets/neo4j-visualização.css

## 🛠️ Tecnologias e Utilização

| Tecnologia | Utilização                                            |
| ---------- | ----------------------------------------------------- |
| **Neo4j**  | Banco de dados orientado a grafos                     |
| **Cypher** | Modelagem e consultas ao grafo                        |
| **Python** | Inspeção, limpeza e preparação dos dados              |
| **Pandas** | Manipulação dos dados                                 |
| **APOC**   | Recursos auxiliares utilizados na construção do grafo |
| **Docker** | Opção de execução local do Neo4j                      |
| **CSS**    | Customização visual                                   |
| **Git**    | Versionamento                                         |
| **GitHub** | Repositório e documentação                            |

## 📂 Estrutura do Repositório

Analise-de-Engajamento/
│
├── Assets/
│   └── neo4j-visualização.css
│
├── Docs/
│   └── modelo-do-grafo.md
│
├── Evidencias/
│   ├── 01-visao-geral-rede.cypher
│   ├── 02-cluster-moda.cypher
│   └── 03-top-influenciadores-tabela.cypher
│
├── Problemas/
│   ├── 01-encoding-caracteres.cypher
│   ├── 02-hastags-invalidas.cypher
│   ├── 03-performance-follow.cypher
│   └── 04-memoria-grafos-grandes.bash
│
├── Queries/
│   ├── 01-top-influenciadores.cypher
│   ├── 02-comunidades-hastags.cypher
│   ├── 03-engajamento-localização
│   ├── 04-recomendacao-conteudo.cypher
│   ├── 05-gap-mercado.cypher
│   └── 06-caminhos-influencia.cypher
│
├── Scripts/
│   ├── carga-neo4j.cypher
│   ├── execucao-passo-a-passo.bash
│   └── preparacao-dataset.py
│
└── README.md

## ▶️ Como Executar

1. Obtenha o projeto

git clone https://github.com/MCLG1661/Analise-de-Engajamento.git
cd Analise-de-Engajamento

2. Prepare o ambiente Python

Instale as dependências necessárias para preparação dos dados.

Exemplo:

pip install pandas numpy

3. Prepare o dataset

Coloque o arquivo utilizado pelo projeto no diretório de execução com o nome esperado:

instagram_usage_lifestyle.csv

Depois execute:

python Scripts/preparacao-dataset.py

Será criado:

instagram_clean.csv

4. Configure o Neo4j

Utilize uma instância local ou ambiente compatível com Neo4j.

O repositório inclui um roteiro auxiliar:

Scripts/execucao-passo-a-passo.bash

5. Carregue o grafo

Execute o conteúdo de:

Scripts/carga-neo4j.cypher

6. Execute as análises

As consultas analíticas estão disponíveis em:

Queries/

Cada arquivo aborda uma dimensão diferente do problema de Social Media Analytics.

## 💡 Competências Demonstradas

Data & Graph Analytics
Neo4j
Cypher
Graph Databases
Graph Data Modeling
Network Analysis
Data Cleaning
Data Quality
Python
Pandas
Marketing Analytics
Social Media Analytics
Influencer Analysis
Engagement Analysis
Community Analysis
Content Recommendation
Market Opportunity Analysis
Audience Segmentation
Business Insights
Engenharia e Organização
Data Pipeline
Performance Analysis
Tratamento de erros
Organização de código
Git
GitHub

## 🚀 Possíveis Evoluções

Uma evolução natural do projeto seria incorporar técnicas de Graph Data Science, incluindo:

PageRank;
Louvain Community Detection;
Degree Centrality;
Betweenness Centrality;
Node Similarity;
Community Detection;
Influencer Scoring;
Link Prediction.

Outras possibilidades:

dashboard interativo;
Streamlit;
API;
sistema de recomendação;
análise temporal;
monitoramento de campanhas;
detecção de tendências;
Machine Learning;
dados reais de relacionamento;
comparação entre segmentos;
visualização interativa da rede.

## ⚠️ Limitações

Este projeto possui finalidade educacional e analítica.

Parte da rede é construída a partir de regras e relacionamentos simulados para permitir a exploração de conceitos de bancos de dados em grafos.

Portanto:

os resultados não representam comportamento real de usuários específicos;
relações sociais inferidas não devem ser interpretadas como conexões observadas;
métricas e resultados servem principalmente para demonstrar técnicas de Graph Analytics.
🎓 Contexto

Projeto desenvolvido durante o Bootcamp Neo4j — Análise de Dados com Grafos, da DIO.

Disciplina: Modelagem de Bancos Baseados em Grafos
Professor: Matheus Ferreira
Período: Primeiro semestre de 2026
Entrega: 16/03/2026

## 👨‍💻 Autor

Marcus Guedes

Marketing | Data Science | Inteligência Artificial | Gestão de Projetos

GitHub: MCLG1661

⭐ Graph Analytics aplicado a Marketing: transformando conexões em insights de negócio.

⭐ Graph Analytics aplicado a Marketing: transformando conexões em insights de negócio.

