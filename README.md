# 📌 Pipeline de Dados End-to-End com AWS - PNAD COVID-19 —

Este projeto implementa um pipeline de dados end-to-end utilizando serviços da Amazon Web Services (AWS) para ingestão, transformação e análise dos dados da PNAD COVID-19, disponibilizados pelo IBGE.

O trabalho integra práticas de engenharia de dados e análise exploratória para geração de datasets enriquecidos e tratados, além da geração de insights relevantes.

---

## 🚀 Visão Geral

O pipeline segue uma arquitetura em camadas (Medallion Architecture), transformando dados brutos em informações prontas para análise:

- **Ingestão (Raw)**: Upload de arquivos CSV para o Amazon S3  
- **Processamento (ETL)**: Transformações com AWS Glue, utilizando PySpark e catalogando os dados no Glue Data Catalog (aplicação de questionário do IBGE para tradução dos dados)
- **Curadoria (Gold)**: Dados estruturados para consumo analítico e aplicação de engenharia de features
- **Análise (EDA)**: Exploração e geração de insights com Python  

---

## 🏗️ Arquitetura e pipeline de dados

Veja mais detalhes em: [Architecture](docs/architecture.md)

---

## 🛠️ Tecnologias Utilizadas

- PySpark
- AWS S3
- AWS Glue
- AWS Glue Data Catalog
- AWS Amazon Athena
- Google Colab
- Jupyter Notebook
- Python
- Pandas
- Matplotlib
- Seaborn

---

## 📂 Estrutura do Repositório
```bash
.
├── docs/
│   ├── architecture.md
│   └── architecture.png
│
├── eda-notebook/
│   └── covid-pnad-data-exploration.ipynb
│
├── src/
│   └── etl/
│       ├── ingest/
│       │   └── covid-pnad-ETL-job-csv-to-raw.ipynb
│       └── transform/
│           └── covid-pnad-notebook-ETL-job-raw-to-gold.ipynb
│
├── .gitignore
└── README.md
```

---

## 📊 Análise Exploratória (EDA)

📌 Desenvolvido como parte da pós-graduação em Data Analytics pela FIAP, a análise tem foco em identificar:

- Perfis com maior risco de agravamento  
- Pressão potencial sobre a rede hospitalar  
- Barreiras de acesso ao atendimento  
- Comportamentos associados ao aumento de casos  
- Recomendações para planejamento hospitalar em cenários de surto 
- Taxas de infecção por região   
- Perfis comportamentais de risco  
- Indicadores de gravidade e acesso à saúde
- Relação entre fatores socioeconômicos e contágio   

---

## 📊 Principais Insights

- Os sintomas mais frequentes foram dor de cabeça, nariz entupido e tosse  
- A gravidade está concentrada em pacientes idosos e/ou com comorbidades  
- O número de sintomas é um forte indicador de necessidade de internação  
- Existe grande perda entre “ter sintomas” e “buscar atendimento”  
- A maior pressão hospitalar ocorre no atendimento inicial, e não necessariamente na internação  
- O risco comportamental ajuda a antecipar movimentos de aumento da positividade  
- Pacientes com 5 ou mais sintomas apresentam maior probabilidade de evolução grave  

---

## 🏥 Recomendações Geradas

Com base na análise, as principais recomendações para hospitais são:

- Reforçar a triagem utilizando idade, sintomas e comorbidades  
- Priorizar o monitoramento de grupos vulneráveis  
- Reservar leitos específicos para idosos  
- Acompanhar indicadores de internação e ventilação  
- Planejar capacidade hospitalar de forma preditiva  
- Direcionar campanhas de conscientização conforme o perfil de risco regional  

---

## 🎯 Principais Aprendizados

- Construção de pipelines de dados em cloud AWS (S3, Glue, Glue Data Catalog, Athena)
- Uso do AWS Glue, para ETL escalável  
- Modelagem em arquitetura por camadas (raw → silver → gold)  
- Aplicação de engenharia de features e análise exploratória com dados reais

---

## 📌 Etapas futuras / próximas etapas

- Implementar validação de qualidade de dados  
- Adicionar orquestração (ex: Airflow)  
- Criar dashboards (Power BI / Tableau)  
- Otimizar processamento com Spark

---

## 👥 Integrantes

- Ariany Bertoncello  
- Érica Bugni  
- João Vitor Braga  
- Juliana Moretto  
- Willer Stern  
