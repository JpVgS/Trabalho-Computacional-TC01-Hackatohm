# Trabalho 01: Detecção de Anomalias em Transporte de Motores

Este repositório contém a implementação do "núcleo de código funcional"  para o Trabalho 01 da disciplina de Introdução à Inteligência Artificial (Prof. Everthon de Souza Oliveira).

O projeto é um "recorte" do problema do HackatOhm 2025 (`Skid de Transporte para Motores Elétricos`), focando especificamente na criação de um protótipo para o "Agente de IA Integrado" (Seção 8 do `Skid.pdf`).

O objetivo deste núcleo é validar um pipeline mínimo para **detecção de anomalias (choques) em dados de vibração**, utilizando um baseline simples e uma variação com `scikit-learn`.

## 📂 Estrutura do Repositório
O repositório está organizado para atender aos requisitos de "estrutura mínima de pastas" e "funcionalidade verificável":

```
/
│
├── 📄 TC_01.ipynb
│
├── 📁 outputs/
│   ├── 📊 grafico_dados.png
│   └── 📊 grafico_resultados.png
│
└── 📄 README.md
```

  * **`TC_01.ipynb`**: Este é o notebook Google Colab que contém todo o código, a análise e o "minirrelatório"  detalhado, explicando o problema, os dados, os métodos e os resultados.
  * **`outputs/`**: Contém os "outputs exemplares"  (gráficos) gerados pela execução do notebook.
  * **`README.md`**: Este arquivo.

## 🚀 Como Executar (Instruções)

A forma mais fácil de verificar este trabalho é usando o Google Colab, que já possui todas as dependências instaladas (`numpy`, `pandas`, `sklearn`).

1.  **Clique no link abaixo** para abrir o notebook diretamente no Google Colab:

    ```
    https://colab.research.google.com/github/JpVgS/Trabalho-Computacional-TC01-Hackatohm/blob/main/TC_01.ipynb
    ```

2.  Uma vez no Colab, clique em **"Ambiente de execução"** (Runtime) no menu superior.

3.  Selecione **"Executar tudo"** (Run all).

O notebook irá executar todas as células em ordem:

1.  Gerará os dados sintéticos (vibração normal + choques).
2.  Treinará e executará o modelo Baseline (Limiar 3-Sigma).
3.  Treinará e executará o modelo Variação (`IsolationForest`).
4.  Gerará os relatórios de métrica (`classification_report`).
5.  Exibirá os gráficos de dados e resultados.

## 📈 Resultados Esperados

A execução do notebook irá gerar os gráficos de análise, que também estão salvos na pasta `outputs/`.

Os resultados das métricas (F1-score) demonstram que o modelo de variação (`IsolationForest`) é significativamente superior ao baseline para a detecção dos "Choques Transientes Severos", validando o conceito proposto no `Skid.pdf`.

