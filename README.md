<h1 align="center"> Atividade de Inteligência Artificial</h1>

**Disciplina:** Inteligência Artificial<br>
**Professor:** Ronierison de Souza Maciel<br>
**Aluno:**  Yuri Alves Moreira e Glauber Lima Margem Simplício<br>
**Curso:** Sistemas de Informação – VI Período, Noturno<br>

---

### 🎯 Objetivo da Atividade

Implementar e comparar algoritmos de classificação supervisionada utilizando um dataset real, aplicando técnicas de pré-processamento, modelagem e avaliação de desempenho.

---

### 📊 Dataset Escolhido

**Fonte:** `sklearn.datasets.load_breast_cancer`  

**Descrição:**  
O dataset contém **569 amostras de exames de mama**. Cada amostra descreve características computadas a partir da imagem digitalizada de uma punção aspirativa por agulha fina (FNA) de uma massa mamária.  

**Tamanho:** 569 amostras × 30 atributos (features).  

**Variável alvo:**  
- **Maligno (0)**  
- **Benigno (1)**  

**Principais features:**  
- raio médio, textura, perímetro, área, suavidade, compacidade, concavidade, simetria, dimensão fractal (média, erro padrão e pior valor de cada uma).  

**Justificativa da escolha:**  
É um dataset clássico, amplamente usado em experimentos de Machine Learning, de tamanho moderado, balanceado entre classes e com atributos contínuos. Por isso, é ideal para testar diferentes algoritmos de classificação supervisionada.

---

## 📈 Resultados Obtidos

***Decision Tree:***

```
Decision Tree: - Acurácia: 0.91228, Precisão: 0.91367
Precisao:0.91367
Matriz de Confusão:
[[38  4]
 [ 6 66]]



               precision    recall  f1-score   support

           0       0.86      0.90      0.88        42
           1       0.94      0.92      0.93        72

    accuracy                           0.91       114
   macro avg       0.90      0.91      0.91       114
weighted avg       0.91      0.91      0.91       114

```

***KNN:***

```
KNN: - Acurácia: 0.91228, Precisão: 0.91367
Precisao:0.91367
Matriz de Confusão:
[[38  4]
 [ 6 66]]



               precision    recall  f1-score   support

           0       0.86      0.90      0.88        42
           1       0.94      0.92      0.93        72

    accuracy                           0.91       114
   macro avg       0.90      0.91      0.91       114
weighted avg       0.91      0.91      0.91       114

***Logistic Regression:***

```
Logistic Regression: - Acurácia: 0.96491, Precisão: 0.96518
Precisao:0.96518
Matriz de Confusão:
[[39  3]
 [ 1 71]]



               precision    recall  f1-score   support

           0       0.97      0.93      0.95        42
           1       0.96      0.99      0.97        72

    accuracy                           0.96       114
   macro avg       0.97      0.96      0.96       114
weighted avg       0.97      0.96      0.96       114
```

---

## 📝 Conclusão

O modelo com melhor desempenho no dataset **Breast Cancer** foi a `Logistic Regression`, que obteve a maior acurácia entre os algoritmos testados.  

Esse resultado é coerente, pois o dataset apresenta variáveis contínuas e classes relativamente bem separadas linearmente, favorecendo modelos lineares.  

Para melhorar o desempenho de algoritmos como o KNN e a Decision Tree, seriam úteis:  
- **Normalização dos dados**, fundamental para o KNN, já que utiliza medidas de distância.  
- **Ajuste de hiperparâmetros** (ex.: profundidade da árvore, número de vizinhos no KNN).  
- **Validação cruzada**, garantindo uma avaliação mais robusta dos modelos.  

---

## 💻 Como Executar

### Clone este repositório:
```bash
git clone https://github.com/moreirayurieada/Notebook.git
```

### Instale as dependências:
```bash
pip install -r requirements.txt
```

### Execute o notebook:
```bash
jupyter notebook exercicio.ipynb
```