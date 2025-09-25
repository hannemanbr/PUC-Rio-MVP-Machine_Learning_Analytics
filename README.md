# ✈️ PUC-Rio MVP: Machine Learning & Analytics
## Classificação de Gravidade de Ocorrências Aeronáuticas

**Autor:** Thomas Alves de Souza Abrantes

---

Este repositório contém a entrega do **MVP (Produto Mínimo Viável)** da Sprint de Machine Learning & Analytics da Pós-Graduação em Ciência de Dados e Analytics na **PUC-Rio**.

---

### 💡 Objetivo do Projeto

O objetivo principal deste projeto é criar um **modelo preditivo robusto** capaz de classificar a gravidade de ocorrências aeronáuticas no Brasil em três categorias: **Acidente**, **Incidente Grave** e **Incidente**.

Uma classificação precisa é vital para a segurança operacional, para a correta alocação de recursos de investigação e para o desenvolvimento de políticas preventivas pelo CENIPA.

O modelo utiliza características detalhadas da aeronave e da ocorrência para diferenciar as três classes de forma consistente e com alta confiabilidade, fornecendo uma valiosa análise preditiva para o sistema de segurança aeronáutica.

---

### 💻 Notebook e Código

Todo o desenvolvimento, análise de dados e treinamento do modelo preditivo foram realizados no seguinte notebook do Google Colab:

* **Notebook Google Colab:** `THOMAS_MVP_SPRINT_3_Machine_Learning_&_Analytics.ipynb`

---

### 📊 Base de Dados

Os arquivos foram extraídos do Portal Dados Abertos do Governo Federal e disponibilizados pelo **CENIPA** (Centro de Investigação e Prevenção de Acidentes Aeronáuticos).

* **Link da Fonte:** [Ocorrências Aeronáuticas da Aviação Civil Brasileira](https://dados.gov.br/dados/conjuntos-dados/ocorrencias-aeronauticas-da-aviacao-civil-brasileira)

#### Arquivos Incluídos

| Arquivo | Descrição | Registros |
| :--- | :--- | :--- |
| `aeronave.csv` | Informações detalhadas das aeronaves envolvidas nas ocorrências. | Mais de 13 mil |
| `ocorrencia.csv` | Dados cronológicos e geográficos de cada evento. | Mais de 13 mil |
| `ocorrencia_tipo.csv` | Informações sobre a categoria e taxonomia de cada ocorrência. | Mais de 13 mil |
| `fator_contribuinte.csv` | Fatores humanos, técnicos e operacionais que contribuíram para a ocorrência. | Mais de 8 mil |
| `recomendacao.csv` | Registros das recomendações feitas após as conclusões das investigações. | Mais de 3 mil |
| `modelo_dados.webp` | Diagrama visual do relacionamento entre todos os datasets. | --- |

---

### ⚙️ Conclusão da Modelagem

O modelo final escolhido foi o **LightGBM (Pré-SMOTE)**, devido à sua capacidade superior de discriminação.

O LightGBM demonstrou o melhor equilíbrio entre segurança (baixo erro crítico na previsão de Acidentes) e precisão, sendo o único modelo capaz de classificar corretamente cenários de risco intermediário como **Incidente Grave** nos testes práticos. As *features* de maior peso no modelo foram o **PMD** (Peso Máximo de Decolagem), o **Ano de Fabricação** e a necessidade de **Recomendações** após o evento.
