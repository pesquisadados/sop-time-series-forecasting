# Sales Forecasting & Inventory Intelligence (S&OP)

Este repositório apresenta o desenvolvimento de uma estrutura técnica de **Sales and Operations Planning (S&OP)**. O projeto foca na integração de bases de dados heterogêneas para otimizar o processo de tomada de decisão na cadeia de suprimentos, utilizando modelagem de séries temporais.

## Sobre o Repositório

O objetivo central é a implementação de um pipeline de dados que une o histórico de demanda com níveis de inventário para gerar previsões altamente assertivas. O diferencial deste estudo é a inclusão de variáveis logísticas exógenas que capturam a **"Pressão de Inventário"**, permitindo que o modelo compreenda restrições e excessos de estoque.

---

## Modelos Preditivos Utilizados

O projeto avalia e compara diversos modelos de séries temporais, desde abordagens clássicas até modelos multivariados avançados:

1.  **SES (Simple Exponential Smoothing):** Baseline para séries sem tendência ou sazonalidade.
2.  **Holt (Tendência Linear):** Modelo para séries com crescimento ou declínio constante.
3.  **Holt-Winters (Sazonal):** Modelo triplo-exponencial que captura ciclos sazonais.
4.  **Descomposição Clássica:** Método para isolar Tendência, Sazonalidade e Resíduo de forma aditiva ou multiplicativa.
5.  **Decomposição STL:** Separação robusta de tendência e sazonalidade via LOESS.
6.  **ARIMA:** Modelo autorregressivo integrado de médias móveis. 
7.  **SARIMAX:** Modelo vencedor que utiliza sazonalidade e **variáveis exógenas de logística**.

---

## Tecnologias e Bibliotecas

* **Linguagem:** Python 3.12+
* **Manipulação e ETL:** `Pandas`, `NumPy`
* **Modelagem Estatística:** `statsmodels`, `pmdarima`, `scipy`
* **Visualização:** `Matplotlib`
* **Ambiente:** Google Colab / Jupyter Notebook

---

## Como Executar o Projeto

Este projeto foi desenhado para ser executado no ambiente **Google Colab**. Siga os passos abaixo:

### 1. Preparação dos Dados
Certifique-se de que as bases de dados estão localizadas no seu Google Drive no caminho especificado no código (`/content/drive/MyDrive/estudo/dados`). As bases necessárias são:
* `base_completa_vendas_orcamento.xlsx`
* `estoque_diario_cd_2022.csv`
* `estoque_diario_rede_2022.csv`

### 2. Instalação de Dependências
Ao abrir o notebook, a primeira célula de código realizará a instalação de bibliotecas não nativas
