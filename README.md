# 🧼 Análise e Limpeza de Dados de Vendas - MegaSuper

Este projeto tem como objetivo realizar uma limpeza completa, padronização e análise de dados de uma base de vendas fictícia da empresa **MegaSuper**. Através de técnicas de pré-processamento e mineração de dados, foram extraídos insights úteis e regras de associação entre produtos mais frequentemente comprados juntos.

---

## 📁 Estrutura do Projeto

- `vendas_modificado.csv`: Arquivo contendo os dados brutos de vendas.
- `limpeza_vendas.ipynb`: Notebook com todo o processo de limpeza e análise.
- `README.md`: Este arquivo com as instruções e descrição do projeto.

---

## ⚙️ Tecnologias Utilizadas

- Python 3
- Pandas
- NumPy
- MLxtend (Apriori e regras de associação)
- Jupyter Notebook

---

## 🔍 Etapas Realizadas

1. **Importação e Visualização Inicial**
   - Leitura da base de dados
   - Análise dos tipos de dados e valores ausentes

2. **Limpeza e Padronização**
   - Conversão da coluna `valor` para tipo numérico
   - Padronização de datas e horários
   - Correção de colunas que deveriam ter o mesmo valor dentro do mesmo `id_da_compra`
   - Recalculo da coluna `total` (`valor * quantidade + frete`)
   - Transformação de valores negativos em positivos
   - Remoção de caracteres especiais em nomes de produtos

3. **Tratamento de Outliers**
   - Detecção de valores fora da curva (IQR)
   - Substituição por `NaN` e preenchimento com média por produto

4. **Mineração de Dados com Apriori**
   - Transformação de dados para formato transacional
   - Aplicação do algoritmo Apriori
   - Geração de regras de associação com base em suporte, confiança e lift

---

## 📊 Resultados

Foram geradas regras de associação entre produtos com alto lift e suporte, indicando padrões de compra relevantes para estratégias de vendas combinadas. Além disso, a base de dados foi completamente padronizada e está pronta para visualizações, dashboards ou treinamentos de modelos preditivos.

---

## 🚀 Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
