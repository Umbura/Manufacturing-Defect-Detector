<div align="center">

# Detecção de Produtos Fora do Padrão com PaDiM

### Controle de Qualidade Automatizado

<!-- LANGUAGE SWITCHER -->
[![Read in English](https://img.shields.io/badge/Read%20in-English-0077B5?style=for-the-badge&logo=google-translate&logoColor=white)](README.md)

<!-- TECH STACK BADGES -->
<p>
  <img src="https://img.shields.io/badge/Python-3.9%2B-blue" alt="Python 3.9+">
  <img src="https://img.shields.io/badge/TensorFlow-2.15-orange" alt="TensorFlow 2.15">
  <img src="https://img.shields.io/badge/Accuracy-98%25-green" alt="Accuracy 98%">
</p>

<!-- MAIN IMAGE -->
<img src="https://github.com/Umbura/Deteccao-de-Produtos-Fora-do-Padrao-de-Fabricacao/raw/main/samples-assets/samples.gif" alt="Demonstração PaDiM" width="100%">

*Demonstração do modelo identificando garrafas fora do padrão de fabricação.*

</div>

---

## Sobre o Projeto
O projeto foi desenvolvido para fins acadêmicos e educacionais, com o propósito de reproduzir e aplicar a metodologia proposta no artigo **“PaDiM: a Patch Distribution Modeling Framework for Anomaly Detection and Localization”** (Defard et al., 2020).

O objetivo central é explorar a metodologia PaDiM no contexto de inspeção visual industrial, aplicando-a à detecção de produtos fora do padrão de fabricação.

A abordagem baseia-se em **one-class learning**, onde o modelo é treinado exclusivamente com imagens de produtos "perfeitos". Isso o torna ideal para cenários industriais, onde defeitos são raros e podem assumir formas imprevisíveis.

O processo consiste em:
1.  Utilizar uma CNN (**ResNet50**) para aprender as características visuais profundas de um produto padrão.
2.  Modelar estatisticamente essa "normalidade" para cada parte do produto.
3.  Durante a inspeção, comparar um novo produto com o modelo estatístico aprendido e calcular um **score de anomalia**. Scores altos indicam um produto defeituoso.

Este repositório contém a implementação completa em Python, TensorFlow e Keras, desde o pré-processamento até a avaliação final.

---

## Resultados

A implementação otimizada alcançou um desempenho excepcional na detecção de garrafas com defeito, validando a eficácia do método.

*   **AUC-ROC:** **0.9968**
*   **Acurácia (com limiar otimizado):** **98%**

<div align="center">
  <img src="https://github.com/Umbura/Deteccao-de-Produtos-Fora-do-Padrao-de-Fabricacao/raw/main/samples-assets/samples.gif" alt="Amostras de Detecção" width="80%">
  <p><em>Visualização das máscaras de calor indicando a localização exata das anomalias.</em></p>
</div>

> *Nota: Durante a fases de testes batizei o programa de Pandora. Onde inicialmente, tente utilizar apenas CNN para a detecção o resultado foi de F1- 0.76 na categoria Good e 0.90 em anomaly. O que não é um resultado ruim, mas considerando uma aplicação em industria é pessimo, pois a empresa estaria jogando dinheiro fora.
---

## Tecnologias Utilizadas

*   **Linguagem:** Python 3.9+
*   **Frameworks de Machine Learning:** TensorFlow, Keras, Scikit-learn
*   **Bibliotecas de Processamento:** NumPy, SciPy, OpenCV
*   **Visualização:** Matplotlib, Seaborn

---

## Como Executar

### Pré-requisitos
*   Python 3.9 ou superior.
*   Dataset **MVTec AD** (especificamente a categoria "bottle").

### Instalação e Execução
1.  **Clone este repositório:**
    ```bash
    git clone https://github.com/Umbura/Deteccao-de-Produtos-Fora-do-Padrao-de-Fabricacao.git
    ```
2.  **Instale as dependências:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Execute o Notebook:**
    Abra e execute o arquivo `main.ipynb`.

---

## Créditos e Referência

Este projeto é uma implementação do trabalho acadêmico original dos autores do PaDiM.

*   **Artigo Científico:** Defard, T., et al. (2020). *PaDiM: A Patch Distribution Modeling Framework for Anomaly Detection and Localization*. [arXiv:2011.08785](https://arxiv.org/abs/2011.08785).
*   **Dataset:** [MVTec AD - Anomaly Detection Dataset](https://www.mvtec.com/company/research/datasets/mvtec-ad)

---

## Licença

Distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
