# Clusterização de eventos adversos a medicamentos para artrite reumatoide em base nacional de farmacovigilância

Este repositório contém o código-fonte e a metodologia analítica utilizada no estudo sobre o perfil de segurança dos **Medicamentos Modificadores do Curso da Doença (DMARDs)** para **Artrite Reumatoide**, utilizando dados de um sistema nacional de farmacovigilância.

---

## 📋 Resumo do Projeto

O objetivo desta análise foi identificar padrões de similaridade nos perfis de eventos adversos de **10 fármacos** (biológicos e sintéticos alvo-específicos) por meio de técnicas de aprendizado de máquina não supervisionado (**K-Means Clustering**).

A análise processou:

- 23.653 notificações únicas  
- 58.893 associações fármaco-evento  

Essas associações foram categorizadas de acordo com:

- Gravidade  
- Complexidade clínica  
- Distribuição sistêmica (MedDRA SOCs)  

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Python >=3.10  
- **Banco de Dados:** DuckDB >=0.9  

**Bibliotecas de Análise:**
- pandas >=2.0  
- numpy >=1.24  
- scipy >=1.10  

**Machine Learning:**
- scikit-learn >=1.3 (K-Means, StandardScaler)  

**Visualização:**
- matplotlib >=3.7  
- seaborn >=0.12  

---

## 📂 Estrutura do Repositório

```
├── analise_clusters_dmards.ipynb
├── requirements.txt
└── README.md
```


---

## 🚀 Como Reproduzir a Análise

### 1. Preparação do Ambiente

```bash
pip install -r requirements.txt
```

---

### 2. Preparação dos Dados

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

---

### 3. Execução da Análise

Execute o notebook principal:

```bash
jupyter notebook analise_clusters_dmards.ipynb
```

### 4.  Citação

As informações completas de citação serão disponibilizadas após o processo de revisão por pares.
