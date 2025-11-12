# Detecção de Produtos Fora do Padrão de Fabricação com PaDiM

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.15-orange.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

Implementação do framework PaDiM para detecção e localização de defeitos em produtos industriais, demonstrando sua aplicação prática no controle de qualidade automatizado.

![Demonstração do PaDiM](assets/padim_demo.gif)
*Demonstração do modelo identificando garrafas fora do padrão de fabricação.*

---

##  Sobre o Projeto

O projeto foi desenvolvido para fins acadêmicos e educacionais, com o propósito de reproduzir e aplicar a metodologia proposta no artigo
“PaDiM: a Patch Distribution Modeling Framework for Anomaly Detection and Localization”
(Thomas Defard, Aleksandr Setkov, Angélique Loesch e Romaric Audigier, Université Paris-Saclay, 2020).
O objetivo central deste trabalho é explorar e implementar a metodologia PaDiM no contexto de inspeção visual industrial, aplicando-a ao problema de detecção de produtos fora do padrão de fabricação.

A metodologia é baseada em *one-class learning*, onde o modelo é treinado exclusivamente com imagens de produtos "perfeitos". Isso o torna ideal para cenários industriais, onde defeitos são raros e podem assumir formas imprevisíveis.

O processo consiste em:
1.  Utilizar uma CNN (ResNet50) para aprender as características visuais profundas de um produto padrão.
2.  Modelar estatisticamente essa "normalidade" para cada parte do produto.
3.  Durante a inspeção, comparar um novo produto com o modelo estatístico aprendido e calcular um **score de anomalia**. Scores altos indicam um produto fora do padrão.

Este repositório contém o notebook com a implementação completa em Python, TensorFlow e Keras, desde o pré-processamento até a avaliação final, alcançando resultados de alta precisão.

###  Resultados

A implementação otimizada alcançou um desempenho excepcional na detecção de garrafas com defeito:

*   **AUC-ROC:** **0.9968**
*   **Acurácia (com limiar otimizado):** **98%**

---

##  Tecnologias Utilizadas

*   **Linguagem:** Python
*   **Frameworks de Machine Learning:** TensorFlow, Keras, Scikit-learn
*   **Bibliotecas:** NumPy, SciPy, OpenCV, Matplotlib, Seaborn

---

##  Como Executar

### Pré-requisitos
*   Python 3.9+
*   Dataset **MVTec AD** (categoria "bottle").

### Instalação e Execução
1.  Clone este repositório.
2.  Instale as dependências com `pip install -r requirements.txt`.(opcional)
3.  Abra e execute o notebook `main.ipynb`.

---

## 📜 Créditos e Referência

Este projeto é uma implementação do trabalho acadêmico original dos autores do PaDiM.

*   **Artigo Científico:** Defard, T., et al. (2020). *PaDiM: A Patch Distribution Modeling Framework for Anomaly Detection and Localization*. [arXiv:2011.08785](https://arxiv.org/abs/2011.08785).
*   **MVTec Anomaly Detection (MVTec AD).**[MVTec AD - Anomaly Detection Dataset](https://www.mvtec.com/company/research/datasets/mvtec-ad)**
---

## 📄 Licença

Distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
