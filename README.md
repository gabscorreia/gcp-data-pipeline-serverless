# Pipeline de Dados Serverless End-to-End

[![GCP](https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)](https://cloud.google.com/)
[![Python](https://img.shields.io/badge/PYTHON-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![BigQuery](https://img.shields.io/badge/BIGQUERY-669DF6?style=for-the-badge&logo=google-cloud&logoColor=white)](https://cloud.google.com/bigquery/)
[![Git](https://img.shields.io/badge/GIT-F05032?style=for-the-badge&logo=git&logoColor=white)](https://git-scm.com/)

---

## 📌 Visão Geral do Projeto

Este repositório contém um projeto completo de engenharia de dados desenvolvido com **Google Cloud Platform (GCP)** e **Python**. O objetivo principal é implementar um pipeline analítico robusto seguindo a **Arquitetura Medalhão** (Bronze ➔ Silver ➔ Gold), utilizando o **Google BigQuery** para armazenamento e processamento eficiente via SQL, aplicando boas práticas de desenvolvimento (*Clean Code*) e versionamento de código.

---

## 🏗️ Arquitetura do Projeto

O pipeline foi estruturado em camadas no BigQuery, garantindo rastreabilidade, limpeza rigorosa dos dados e alta performance nas consultas analíticas:

```text
[ Fontes de Dados / CSV ] ---> [ Camada Bronze (Dados Brutos / Raw) ]
                                          |
                                          v
[ Camada Gold (Agregações de Negócio) ] <--- [ Camada Silver (Limpeza e Tipagem) ]
                                          |
                                          v
                       [ Consultas Analíticas via SQL / BigQuery ]
