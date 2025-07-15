# Reconhecimento de Sinais de Trânsito Alemães com HOG e SVM

Este projeto utiliza técnicas clássicas de Visão Computacional para classificar sinais de trânsito do conjunto de dados **GTSRB (German Traffic Sign Recognition Benchmark)**. O pipeline implementado combina extração de características com HOG e classificação com SVM.

## Objetivo

Construir um sistema capaz de reconhecer automaticamente 43 tipos de sinais de trânsito alemães, simulando um cenário de carro autônomo.

## Etapas do Projeto

1. **Download do Dataset**
   - Utiliza o [KaggleHub](https://github.com/kagglehub/kagglehub) para baixar o dataset: `meowmeowmeowmeowmeow/gtsrb-german-traffic-sign`.
   - Estrutura esperada: pastas por classe dentro de `Train`.

2. **Carregamento e Pré-processamento**
   - Leitura das imagens em escala de cinza.
   - Redimensionamento para 64x64 pixels.
   - Organização dos dados e rótulos.

3. **Extração de Características**
   - Utilização do descritor HOG (`skimage.feature.hog`) para cada imagem.
   - Visualização das representações HOG.

4. **Treinamento do Classificador**
   - Divisão dos dados em treino e teste (80/20, estratificado).
   - Treinamento de um SVM linear (`LinearSVC` do scikit-learn).

5. **Avaliação**
   - Cálculo da acurácia e relatório de classificação detalhado.
   - Visualização de exemplos de acertos e erros do modelo.

## Principais Resultados

- **Acurácia Geral:** ~97%
- **Desempenho por Classe:** F1-score acima de 0.99 para várias classes; algumas classes apresentam desafios (ex: classe 2, 5, 1).
- **Visualização:** Exemplos de classificações corretas e incorretas exibidos para análise qualitativa.

## Como Executar

1. Instale as dependências:
   ```
   pip install kagglehub scikit-image scikit-learn opencv-python matplotlib numpy
   ```
2. Baixe o dataset do Kaggle conforme instruções do notebook.
3. Execute o notebook [projeto_reconhecimento_sinais_transito_alemao.ipynb](Projeto_VCAP_GTSRB/projeto_reconhecimento_sinais_transito_alemao.ipynb) em ambiente Jupyter.

## Requisitos

- Python 3.7+
- kagglehub
- scikit-image
- scikit-learn
- opencv-python
- matplotlib
- numpy

## Autor

Projeto desenvolvido por Marcos Vinicius da Silva para estudo de reconhecimento de padrões visuais em sinais de trânsito.

---