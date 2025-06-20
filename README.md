# Benchmark de Séries Temporais

# 📊 Projeto: Benchmark de Modelos de Séries Temporais

## 📝 Introdução

Este projeto tem como objetivo realizar um **benchmark de modelos de previsão de séries temporais**, comparando o desempenho de algoritmos clássicos e modernos na previsão da produção de leite de uma indústria de laticínios. 
A ideia é avaliar, via aplicação web feita em Gradio, diferentes abordagens em cenários reais para ajudar a escolher o modelo mais adequado para aplicações futuras de previsão

---

## 📊 Dados

Os dados utlizados são da produção mensal de leite de uma indústria de laticínios


### Etapas realizadas:
- Importação das bibliotecas necessárias
- Uploado do arquivo CSV
- Definição dos parâmetros de previsão
- Criação das funções que vão definir cada um dos modelos para previsão
- Gráfico para avaliação dos modelos com melhor poder preditivo
- Criação de Aplicação Web do Benchmark com Gradio

---

## 🤖 Modelagem Preditiva

Modelos utilizados:
- `Naive`
- `Mean` 
- `Drift` 
- `Hot-Winters`
- `ARIMA` 

Cada modelo foi ajustado individualmente para prever os próximos `steps_ahead` da série com base no histórico de `window_size`.

---

## 🔍 Principais Insights


- **Modelos tradicionais como Holt e Holt-Winters Additive (HW Additive) demonstraram ótimo desempenho**, principalmente ao lidar com séries que contêm tendência e sazonalidade;
- O modelo **ARIMA teve desempenho satisfatório ao capturar a tendência**, mas sua limitação em lidar com sazonalidade foi visível — o uso de um modelo sazonal como **SARIMA** poderia melhorar os resultados.
- Modelos como `Drift`, `Mean` e `Naive` apresentaram **baixa capacidade preditiva**, sendo úteis apenaspara fins de comparação.
- A visualização final evidencia que **modelos que incorporam sazonalidade** performam melhor em séries temporais com ciclos regulares.


---

## 📈 Visualizações

- Visualizações das séries utilizadas no benchmark

---

## 🛠️ Ferramentas Utilizadas

- **Python** – Linguagem principal  
- **Pandas / NumPy** – Manipulação e análise de dados  
- **Matplotlib / Seaborn / Plotly** – Visualização gráfica  
- **Statsmodels** – Modelos estatísticos de previsão  
- **Gradio** – Criação de interface web interativa  
- **Jupyter Notebook** – Ambiente de desenvolvimento


---

## 🧠 Conclusão

O projeto demonstrou que:

- **Modelos clássicos como Holt e Holt-Winters Additive (HW Additive) foram os mais eficazes** no benchmark, principalmente por capturarem de forma precisa tanto a tendência quanto a sazonalidade da série;
- O **modelo ARIMA apresentou desempenho razoável**, captando a tendência, mas teve limitações ao tentar capturar os ciclos sazonais — o uso de uma variante que considera fatores sazonais como o **SARIMA** seria mais adequado para esse tipo de série;
- Abordagens simples como `Naive`, `Mean` e `Drift` servem como baselines úteis, mas apresentaram fraco desempenho na presença de padrões sazonais e tendências;
- A análise reforça que **a escolha do modelo deve ser orientada pela estrutura da série temporal**, como a presença ou não de sazonalidade e tendência;
- A construção de um **benchmark padronizado** entre modelos foi essencial para identificar os pontos fortes e fracos de cada abordagem;
- Por fim, a criação de uma **aplicação interativa com Gradio** tornou o projeto acessível e aplicável, permitindo que diferentes usuários testem os modelos em tempo real, mesmo sem conhecimento técnico avançado.


---


## 🔄 Próximos Passos

- Adicionar novos modelos como:
  - `XGBoost` com engenharia de features temporais
  - `AutoETS` e `AutoARIMA`
- Testar em séries reais de domínios como vendas, energia, clima

---

🧑‍💻 **Autor e Contato**

**Higor Roberto Coutinho Caetano**  
**LinkedIn**: [https://www.linkedin.com/in/higor-caetano-049521136/](https://www.linkedin.com/in/higor-caetano-049521136/)  
**E-mail**: higorfct@gmail.com
