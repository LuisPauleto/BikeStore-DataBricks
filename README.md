# 🚴 BikeStore Data Lakehouse Pipeline

Pipeline de Engenharia e Análise de Dados **End-to-End** utilizando a **Arquitetura Medalhão** no **Databricks Unity Catalog**, simulando um ambiente moderno de produção para processamento de vendas e controle de estoque.

---

## 🏗️ Arquitetura do Pipeline

O projeto foi estruturado seguindo os princípios de um **Modern Data Lakehouse**:

* **Landing Zone / Volumes:** Recebimento e armazenamento de dados brutos relacionais (formatos CSV).
* **Bronze Layer:** Ingestão e persistência dos dados brutos no formato **Delta Lake**.
* **Silver Layer:** Higienização de dados via **PySpark** e **Spark SQL**, incluindo tratamento avançado de valores nulos, desduplicação por chaves primárias e compostas, e conversão/padronização de tipos (*casting*).
* **Gold Layer:** Modelagem dimensional em **Star Schema** (tabelas fato e dimensão) otimizada para alta performance em consultas analíticas e consumo no **Power BI**.

---

## 🛠️ Tecnologias e Recursos Utilizados

* **Databricks & Unity Catalog:** Governança, gerenciamento de schemas e armazenamento Delta Lake.
* **PySpark & Spark SQL:** Transformação de dados em larga escala, limpeza e manipulação de DataFrames.
* **dbt (data build tool):** Transformações declarativas e linhagem de dados.
* **CI/CD & Git Integration:** Autenticação e integração contínua do Databricks com o **GitHub via Personal Access Token (PAT)** para versionamento seguro de código.

---

## 📂 Estrutura do Repositório

```text
BikeStore-DataBricks/
│
├── 📂 01_bronze/         # Scripts de Ingestão dos arquivos brutos
├── 📂 02_silver/         # Scripts de Tratamento, Tipagem e Limpeza (PySpark/SQL)
├── 📂 03_gold/           # Modelagem Dimensional (Fatos e Dimensões para BI)
├── 📂 files/             # Arquivos utilizados no projeto
└── 📄 README.md          # Documentação do Projeto
