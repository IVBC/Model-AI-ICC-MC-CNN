# 📊 Avaliação de Modelos Baseados em Mapas de Densidade para Contagem de Pessoas em Imagens Urbanas

Este projeto tem como objetivo **comparar e avaliar duas arquiteturas de redes neurais profundas** aplicadas à tarefa de **contagem de pessoas em imagens** utilizando **mapas de densidade**. O trabalho faz uso do benchmark **ShanghaiTech Dataset - Parte B** para realizar treinamento, validação e teste das abordagens:

- 🔷 **MC-CNN (Multi-Column Convolutional Neural Network)**
- 🔶 **ICC (Inception + Contextual Module + Decoder)**

---

## 📌 Descrição do Problema

A contagem de multidões é um desafio recorrente em visão computacional. Este projeto trata o problema como uma **regressão baseada em mapas de densidade**, onde:

- Cada imagem possui anotações com as coordenadas das pessoas.
- A rede neural aprende a gerar um mapa de densidade.
- A **soma do mapa estimado** indica o número de pessoas previstas.

---

## 🚀 Execução

Você pode executar os experimentos diretamente no **Google Colab**, utilizando os links abaixo:

### 🔷 Notebook do Modelo MC-CNN:
📎 [Abrir no Google Colab](https://colab.research.google.com/drive/1LCn222vd8T62KXhOr2xyPHN-yTspsYZO?usp=sharing)

### 🔶 Notebook do Modelo ICC:
📎 [Abrir no Google Colab](https://colab.research.google.com/drive/1keH59peIK0IPKqP2VZBeeyyh0Uf4qC9M?usp=sharing)

### ✅ Requisitos para rodar:
- Conta Google com acesso ao Google Colab
- Dataset **ShanghaiTech Parte B** salvo no Google Drive
- Autenticação com `drive.mount('/content/drive')` incluída nos notebooks
- Dependências como `torch`, `torchvision`, `opencv`, `scipy` já são instaladas no Colab

---

## 📈 Resultados Obtidos

| Modelo   | MAE (Treino) | MAE (Validação) | MAE (Teste) | Observações                         |
|----------|--------------|------------------|--------------|-------------------------------------|
| MC-CNN   | ~8.5         | ~9.5             | **9.77**     | Simples, eficiente e rápido         |
| ICC      | ~8.7         | ~9.8             | **9.51**     | Arquitetura mais profunda e robusta |

- Ambos os modelos foram treinados por **15 épocas**, utilizando a mesma função de perda combinada (MSE + MAE).
- O modelo **ICC obteve desempenho superior**, com maior estabilidade na validação.
- O **MC-CNN** se mostrou altamente competitivo, com menor complexidade e tempo de treino.

---

## 📚 Organização dos Notebooks

Cada notebook possui:
- 📂 Leitura e visualização do dataset
- 🧠 Definição do modelo
- ⚙️ Treinamento e Validação com métricas
- 📊 Visualização de curvas (Loss e MAE)
- 🧪 Teste com predições reais
- 🔍 Análise dos resultados e comparação com ground truth

---

## 🧾 Conclusão

Este projeto demonstra como arquiteturas distintas — uma clássica e leve (MC-CNN) e outra mais moderna e profunda (ICC) — podem ser aplicadas com sucesso ao problema de contagem de multidões com redes neurais. Ele também destaca os desafios da generalização nesse tipo de tarefa e mostra a importância da análise de métricas e visualização para avaliação de modelos.

---

## 📎 Créditos

- Dataset: [ShanghaiTech Crowd Counting Dataset](https://github.com/desenzhou/ShanghaiTech-Crowd-Counting-Dataset)
- Modelos baseados em artigos clássicos e adaptações de implementações públicas

---

## 📬 Contato

Caso tenha dúvidas ou sugestões, sinta-se à vontade para entrar em contato.

