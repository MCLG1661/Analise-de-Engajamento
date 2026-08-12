# 📱 Análise de Engajamento - Instagram Lifestyle

*Análise de engajamento e influência com Neo4j, Cypher e Python*

![Neo4j](https://img.shields.io/badge/Neo4j-Graph%20Database-4581C3?logo=neo4j&logoColor=white)
![Cypher](https://img.shields.io/badge/Cypher-Graph%20Query-018BFF)
![Python](https://img.shields.io/badge/Python-Data%20Processing-3776AB?logo=python&logoColor=white)
![Graph Analytics](https://img.shields.io/badge/Graph-Analytics-2E8B57)
![Marketing Analytics](https://img.shields.io/badge/Marketing-Analytics-FF6F00)
![Social Media](https://img.shields.io/badge/Social%20Media-Analytics-C13584)
![Neo4j GDS](https://img.shields.io/badge/Neo4j-Graph%20Data%20Science-008CC1)
![DIO](https://img.shields.io/badge/DIO-Neo4j%20Bootcamp-5A0FC8)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

Projeto de **Social Media Analytics baseado em grafos**, desenvolvido para explorar 
relações entre usuários, conteúdos, hashtags, categorias e padrões de engajamento 
em um contexto de Instagram Lifestyle.

A solução utiliza **Neo4j, Cypher e Python** para transformar dados de mídias sociais 
em uma estrutura de relacionamentos capaz de apoiar análises de influência, 
comunidades, engajamento, conteúdo e oportunidades de mercado.

---

## 🎯 Objetivo

Explorar como **Graph Analytics** pode ser aplicado a problemas de Marketing e 
Social Media para identificar padrões que seriam mais difíceis de observar 
utilizando apenas análises tabulares tradicionais.

O projeto trabalha conceitos como :

- Social Media Analytics
- Marketing Analytics
- Graph Databases
- Neo4j
- Cypher
- Influencer Analysis
- Community Analysis
- Engagement Analysis
- Content Recommendation
- Market Gap Analysis
- Network Analysis

---

## 💼 Problema de Negócio

Uma startup de análise de mídias sociais deseja desenvolver um produto capaz de 
gerar insights sobre engajamento e conexões entre usuários em conteúdos relacionados 
ao universo lifestyle.

O domínio inclui temas como :

- Moda
- Viagens
- Fitness
- Alimentação
- Beleza
- Lifestyle

A proposta é utilizar as relações existentes nos dados para responder perguntas 
relevantes para Marketing.

---

## 🧠 Por que utilizar Grafos ?

Mídias sociais são, por natureza, redes de relacionamentos.

```text
Usuário
   ↓
PUBLICA
   ↓
Post
   ↓
UTILIZA
   ↓
Hashtag

Ao mesmo tempo:

Usuário
   ↓
SEGUE
   ↓
Usuário

e:

Post
   ↓
PERTENCE
   ↓
Categoria

```
A modelagem em grafos permite analisar essas relações como uma rede conectada, 
em vez de observar cada elemento isoladamente.

---

## 🕸️ Modelo do Grafo

<img width="800" height="400" alt="ChatGPT Image 12 de ago  de 2026, 15_52_56" src="https://github.com/user-attachments/assets/6c6ff067-38b7-408c-9fac-c26482ab3187" />

---

## 🏗️ Pipeline Analítico

```text
Dataset
   ↓
Preparação dos Dados
   ↓
Python
   ↓
Limpeza / Validação
   ↓
Neo4j
   ↓
Modelagem do Grafo
   ↓
Cypher
   ↓
Graph Analytics
   ↓
Insights de Marketing
```
---

# 🔎 Análises Desenvolvidas

👑 Influenciadores por Categoria

Identificação de usuários relevantes dentro de diferentes segmentos de conteúdo.

Arquivo:

`Query 1: Top Influenciadores por Categoria.cypher`

---

#️⃣ Comunidades de Hashtags

Exploração das relações existentes entre hashtags e conteúdos para identificar 
agrupamentos e padrões temáticos.

Arquivo:

`Query 2: Comunidades de Hashtags.cypher`

---

📍 Engajamento por Localização

Análise das relações entre localização e padrões de engajamento.

Arquivo:

`Query 3: Padrões de Engajamento por Localização.cypher`

---

🎯 Recomendação de Conteúdo

Exploração de conexões do grafo para identificar conteúdos relacionados e 
possibilidades de recomendação.

Arquivo:

`Query 4: Recomendação de Conteúdo Similar.cypher`

---

📈 Gap de Mercado

Análise voltada à identificação de categorias com potencial de oportunidade a 
partir das relações e padrões observados nos dados.

Arquivo:

`Query 5: Análise de Gap no Mercado.cypher`

---

🕸️ Caminhos de Influência

Exploração das conexões entre usuários para compreender possíveis caminhos de 
influência dentro da rede.

Arquivo:

`Query 6: Caminhos de Influência.cypher`

---

## 💡 Insights de Negócio

O projeto foi estruturado para investigar questões relacionadas a:

- Influenciadores que atuam em múltiplas categorias
- Diferenças de engajamento por localização
- Hashtags associadas a maior interação
- Categorias com possível espaço de mercado
- Padrões temporais de engajamento
- Relações de influência entre usuários

Essas análises demonstram como estruturas em grafos podem apoiar decisões relacionadas 
a campanhas, conteúdo, segmentação e estratégias de influência.

---

## 🧹 Tratamento de Problemas Reais

O projeto também documenta desafios encontrados durante a preparação e utilização 
dos dados.

Encoding

Tratamento de caracteres especiais presentes no dataset.

Hashtags

Validação de hashtags vazias ou incorretamente formatadas.

Performance

Análise de problemas relacionados à criação e consulta de relacionamentos.

Memória

Tratamento de limitações de recursos para processamento de grafos maiores.

Essa etapa é importante porque aproxima o projeto de situações encontradas em 
pipelines reais de dados.

---

## 🛠️ Tecnologias

**Neo4j** - Banco de dados orientado a grafos

**Cypher** - Modelagem e consultas

**Python** - Preparação e carga dos dados

**Graph Analytics** - Análise de redes e relacionamentos

**CSS** - Customização de visualizações 

**Git** - Versionamento

**GitHub** - Documentação

---

## 📂 Estrutura do Repositório

```text
Analise-de-Engajamento-no-Instagram-Lifestyle/
│
├── Modelo do Grafo
├── Script de Carga Neo4j.cypher
├── Scripts de Carga Adaptados para o Dataset.py
│
├── Query 1: Top Influenciadores por Categoria.cypher
├── Query 2: Comunidades de Hashtags.cypher
├── Query 3: Padrões de Engajamento por Localização.cypher
├── Query 4: Recomendação de Conteúdo Similar.cypher
├── Query 5: Análise de Gap no Mercado.cypher
├── Query 6: Caminhos de Influência.cypher
│
├── Evidências Visuais - Print 1: Visão Geral da Rede.cypher
├── Evidências Visuais - Print 2: Cluster de Moda.cypher
├── Evidências Visuais - Print 3: Top Influenciadores (Tabela).cypher
│
├── Problemas Reais Encontrados - Problema 1: Encoding dos caracteres especiais.cypher
├── Problemas Reais Encontrados - Problema 2: Hashtags vazias ou mal formatadas.cypher
├── Problemas Reais Encontrados - Problema 3: Performance em relacionamentos de follow.cypher
├── Problemas Reais Encontrados - Problema 4: Memória insuficiente para grafos grandes.bash
│
├── Estilo Personalizado para Melhor Visualização.css
├── Execução Passo a Passo.bash
└── README.md
```
---

## ▶️ Como Executar

1. Prepare o ambiente Neo4j

Configure uma instância compatível do Neo4j.

2. Prepare os dados

Utilize o script Python para tratamento e preparação do dataset.

3. Carregue o grafo

Execute:

`Script de Carga Neo4j.cypher`

4. Explore as análises

Execute individualmente as queries disponíveis no repositório.

Cada consulta aborda uma dimensão diferente do problema de Marketing e Social Media.

---

## 💡 Competências Demonstradas

- Neo4j
- Cypher
- Python
- Graph Databases
- Graph Analytics
- Data Modeling
- Social Media Analytics
- Marketing Analytics
- Influencer Analysis
- Community Analysis
- Engagement Analysis
- Content Recommendation
- Network Analysis
- Data Cleaning
- Data Quality
- Performance Analysis
- Business Insights

---

## 🚀 Possíveis Evoluções

O projeto pode evoluir incorporando:

- Graph Data Science
- Louvain Community Detection
- PageRank
- Centrality Algorithms
- Node Similarity
- Detecção de comunidades
- Influencer Scoring
- Recommendation Systems
- Machine Learning
- Dashboard interativo
- Streamlit
- API
- Monitoramento temporal
- Análise de campanhas
- Detecção de tendências
- Comparação entre segmentos

---

## 🎓 Contexto Acadêmico

Projeto desenvolvido durante o **Bootcamp Neo4j — Análise de Dados com Grafos**, 
da DIO.

**Disciplina:** Modelagem de Bancos Baseados em Grafos  
**Professor:** Matheus Ferreira  
**Período:** Primeiro semestre de 2026  
**Entrega:** 16/03/2026

---

## 👨‍💻 Autor

**Marcus Guedes**

Marketing | Data Science | Inteligência Artificial | Gestão de Projetos

GitHub: MCLG1661  

LinkedIn: Marcus Guedes

