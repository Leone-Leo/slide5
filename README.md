# Atividades de Machine Learning - Semi-supervisionado e Auto-supervisionado

Este repositório contém duas atividades práticas de aprendizado de máquina:

1. **Atividade 1**: Aprendizado Semi-supervisionado (Auto-Treinamento) com SpamBase
2. **Atividade 2**: Aprendizado Auto-supervisionado (Autoencoder) com MNIST

## 📋 Requisitos

### Dependências Python

Instale as dependências necessárias:

```bash
pip install scikit-learn numpy pandas matplotlib seaborn tensorflow jupyter
```

Ou use o arquivo `requirements.txt`:

```bash
pip install -r requirements.txt
```

## 🚀 Como Executar

### 1. Clone o repositório

```bash
git clone https://github.com/leone-leo/slide5.git
cd slide5
```

### 2. Instale as dependências

```bash
pip install -r requirements.txt
```

### 3. Inicie o Jupyter Notebook

```bash
jupyter notebook
```

### 4. Execute os notebooks

- **Atividade 1**: Abra `atividade1_semi_supervisionado.ipynb`
- **Atividade 2**: Abra `atividade2_auto_supervisionado.ipynb`

Execute as células em ordem (Cell > Run All ou Shift+Enter em cada célula).

## 📚 Descrição das Atividades

### Atividade 1 - Semi-supervisionado com SpamBase

**Objetivo**: Melhorar um classificador de spam usando poucos dados rotulados (10%) + pseudo-rotulagem dos dados não rotulados (90%).

**Dataset**: SpamBase (OpenML id=44)
- 57 características numéricas
- Classificação binária: spam vs. não-spam

**O que será feito**:
1. Carregar dados e separar 10% rotulados, 90% não rotulados
2. Treinar baseline (modelo supervisionado com apenas 10% dos dados)
3. Implementar auto-treinamento (self-training):
   - Fazer predições nos dados não rotulados
   - Selecionar predições com alta confiança
   - Adicionar ao conjunto de treinamento
   - Retreinar modelo iterativamente
4. Comparar métricas (F1, precisão, recall)
5. Gerar matriz de confusão e análise de erros

### Atividade 2 - Auto-supervisionado com MNIST

**Objetivo**: Aprender representações sem rótulos via autoencoder e usá-las em tarefas de classificação.

**Dataset**: MNIST
- Imagens 28×28 pixels
- Dígitos de 0 a 9

**O que será feito**:
1. Carregar, normalizar e achatar imagens MNIST
2. Construir e treinar um Autoencoder:
   - Encoder: comprime a imagem para representação latente
   - Decoder: reconstrói a imagem a partir da representação
3. Visualizar imagens originais vs. reconstruídas
4. Usar as representações aprendidas para classificação
5. Comparar classificador com features do autoencoder vs. pixels brutos

## 📂 Estrutura do Repositório

```
slide5/
├── README.md                              # Este arquivo
├── requirements.txt                       # Dependências Python
├── atividade1_semi_supervisionado.ipynb   # Notebook Atividade 1
└── atividade2_auto_supervisionado.ipynb   # Notebook Atividade 2
```

## 🎯 Resultados Esperados

### Atividade 1
- Melhoria significativa de performance usando auto-treinamento
- F1-score do auto-treinamento > F1-score do baseline
- Análise de quais tipos de emails são mais difíceis de classificar

### Atividade 2
- Reconstrução visual de dígitos MNIST
- Demonstração de que features aprendidas sem supervisão podem ser úteis
- Comparação de performance entre diferentes abordagens


