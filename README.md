# 🧼 MegaSuper Vendas – Limpeza de Dados

Este projeto foi desenvolvido com o objetivo de **realizar a limpeza e padronização dos dados de vendas** da empresa fictícia *MegaSuper Vendas*, uma startup de e-commerce que enfrentava diversos problemas de qualidade de dados em seu histórico de transações.

---

## 📊 Objetivo

Transformar um DataFrame desorganizado e inconsistente em um **conjunto de dados limpo, padronizado e pronto para análises avançadas**, como mineração de regras de associação, previsão de demanda e detecção de anomalias.

---

## 🛠️ Etapas da Limpeza Realizadas

### ✅ 1. Verificação e Padronização de Tipos e Formatos

- **Datas e Horas**:
  - Conversão da coluna `data` para o formato `YYYY-MM-DD`
  - Conversão da coluna `hora` para o formato `HHMMSS`
- **Valores Numéricos**:
  - Colunas `valor`, `frete` e `total` foram convertidas de strings com símbolo "R$" para `float`
  - Coluna `quantidade` convertida para tipo numérico

---

### ✅ 2. Tratamento de Inconsistências

- **Valores Ausentes**:
  - Valores nulos na coluna `quantidade` foram preenchidos com `1`
- **Registros Duplicados**:
  - Remoção de duplicatas com base na coluna `id_da_compra` (se necessário)
- **Verificação de Cálculos**:
  - Verificação se `total ≈ valor * quantidade + frete`
  - Correção de registros com cálculos incorretos (se aplicável)

---

## 🗂️ Arquivos

- `limpezaNotebook.ipynb` → Notebook principal com todo o processo de limpeza e análise.
- `vendas_modificado.csv` → CSV "sujo" utilizado.
- `dados_limpos` → CSV limpo, com todas as alterações realizadas.
  
---

## 🚀 Tecnologias

- Python
- Pandas
- Jupyter Notebook

