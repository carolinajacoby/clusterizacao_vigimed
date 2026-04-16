# Clusterização de eventos adversos a medicamentos para artrite reumatoide em base nacional de farmacovigilância.


Este repositório contém o código-fonte e a metodologia analítica utilizada no estudo sobre o perfil de segurança dos **Medicamentos Modificadores do Curso da Doença (DMARDs)** para **Artrite Reumatoide**, utilizando dados do sistema **VigiMed (ANVISA)**.

---

## 📋 Resumo do Projeto

O objetivo desta análise foi identificar padrões de similaridade nos perfis de eventos adversos de **10 fármacos** (biológicos e sintéticos alvo-específicos) por meio de técnicas de aprendizado de máquina não supervisionado (**K-Means Clustering**).

A análise processou:

- **23.653 notificações únicas**
- **58.893 associações fármaco-evento**

Essas associações foram categorizadas de acordo com:

- Gravidade
- Complexidade clínica
- Distribuição sistêmica (**MedDRA SOCs**)

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Python 3.x  
- **Banco de Dados:** DuckDB (processamento de alto desempenho para grandes volumes de dados)  
- **Bibliotecas de Análise:**  
  - pandas  
  - numpy  
  - scipy  
- **Machine Learning:**  
  - scikit-learn (K-Means, StandardScaler)  
- **Visualização:**  
  - matplotlib  
  - seaborn  

---

## 📂 Estrutura do Repositório
```
├── notebooks/
│ └── analise_clusters_dmards.ipynb
│

├── requirements.txt
│ └── Dependências do ambiente
```


---


## 🚀 Como Reproduzir a Análise

### 1. Preparação dos Dados

Os dados utilizados neste estudo são provenientes de um **dataset público nacional de farmacovigilância baseado em notificações espontâneas**.

Para garantir o processo de revisão duplo-cego, detalhes adicionais sobre a fonte foram temporariamente omitidos.

O pipeline segue a arquitetura **Medallion**:

- **Bronze:** Dados brutos extraídos  
- **Silver:**  
  - Remoção de duplicatas  
  - Padronização de princípios ativos (DCI)  
- **Gold:**  
  - Matriz consolidada por fármaco  
  - Variáveis de desfecho  
  - Distribuição sistêmica  

Se este código for útil para sua pesquisa, por favor cite:


