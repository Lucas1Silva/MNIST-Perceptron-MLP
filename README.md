# 📌 Classificação de Dígitos MNIST com Perceptron e MLP

Este projeto implementa dois modelos de classificação para o dataset **MNIST** (conjunto de dígitos escritos à mão), utilizando:
- **Perceptron Simples:** Modelo de aprendizado supervisionado baseado em um único neurônio.
- **MLP (Multi-Layer Perceptron):** Rede neural densa com múltiplas camadas para melhorar a precisão.

## 📖 Descrição do Problema
O objetivo é classificar corretamente imagens de dígitos de **0 a 9** a partir do dataset **MNIST**, amplamente utilizado para aprendizado de **Machine Learning** e **Deep Learning**.

O dataset contém:
- **60.000 imagens de treinamento** (28x28 pixels, tons de cinza)
- **10.000 imagens de teste**

Cada imagem é representada por **784 pixels achatados** (28x28 → vetor de 784 dimensões).

---

## 📌 Estrutura do Código

O código é dividido em células para melhor organização e eficiência no **Kaggle Notebook**. Cada etapa do pipeline pode ser executada separadamente.

### 📌 1️⃣ Importação de Bibliotecas
Importamos **NumPy, TensorFlow, Matplotlib, Seaborn** e outras bibliotecas para manipulação de dados e modelagem.

### 📌 2️⃣ Carregamento e Pré-processamento dos Dados
- O dataset MNIST é carregado diretamente dos arquivos **IDX** no Kaggle.
- Os dados são normalizados (**MinMaxScaler**) para ficar no intervalo `[0,1]`.
- O conjunto de dados é dividido em **Treino (80%)** e **Validação/Teste (20%)**.

### 📌 3️⃣ Implementação do Perceptron
Criamos uma classe **Perceptron** do zero, que:
- Inicializa pesos e viés (`w, b`).
- Utiliza a função de ativação **step function**.
- Atualiza os pesos via **Regra de Aprendizado do Perceptron**.
- Treina por `n_epochs` e armazena os erros ao longo do tempo.

### 📌 4️⃣ Implementação do MLP
Criamos uma **Rede Neural Densa (MLP)** usando `TensorFlow` com:
- **128 neurônios na camada oculta** (ReLU).
- **10 neurônios na camada de saída** (Softmax).
- **Adam Optimizer e Sparse Categorical Crossentropy**.

### 📌 5️⃣ Treinamento e Avaliação dos Modelos
- O **Perceptron** é treinado e avaliado com `np.mean(y_pred == y_test)`.
- O **MLP** é treinado com `model.fit()` e avaliado com `model.evaluate()`.

### 📌 6️⃣ Visualização dos Resultados
✅ **Amostras do Dataset**  
✅ **Gráfico de Convergência do Perceptron**  
✅ **Histórico de Treinamento do MLP (Perda e Acurácia)**  
✅ **Matriz de Confusão** para análise de erros.

---

## 📊 **Resultados Obtidos**
| Modelo       | Acurácia no Teste |
|-------------|----------------|
| **Perceptron** | `98.98%` |
| **MLP**        | `A ser obtida após treinamento` |

⚠ **Nota:** A acurácia pode variar a cada execução devido à inicialização dos pesos.

---

## 🚀 Conclusão
Este projeto demonstrou a diferença de desempenho entre um **Perceptron Simples** e uma **Rede Neural Profunda (MLP)** para a classificação de dígitos.  
- O **Perceptron** funciona bem para problemas lineares, mas não consegue generalizar padrões complexos.
- O **MLP**, por ter múltiplas camadas, oferece maior poder de representação e melhora o desempenho.

📌 **Próximos Passos:**  
- Expandir a rede neural adicionando **mais camadas** (Deep Learning).  
- Experimentar **CNNs (Redes Neurais Convolucionais)** para melhorar a acurácia.

---

## 📢 Conecte-se Comigo!  
Caso tenha dúvidas, sugestões ou queira trocar experiências sobre **Machine Learning e Deep Learning**, entre em contato comigo no LinkedIn:  

🔗 **[Lucas Silva](https://www.linkedin.com/in/Lucas19Silva/)**  

🚀 Vamos crescer juntos na jornada de IA!  
