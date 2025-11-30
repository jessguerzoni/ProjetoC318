
## C318: Previsão de Desempenho Escolar 

**Aluno:** Jéssica Guerzoni - 1801 - GEC
**Tema:** Desempenho estudantil com base em dados educacionais
**Dataset:** [Students Performance Dataset (Kaggle)](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)

---

##  1. Objetivo 

Fazer uma análise de modo a conseguir prever o mais próximo possível as chances de aprovação baseados nos requisitos abaixo:


* Gênero
* Escolaridade dos pais
* Curso preparatório
* Grupo étnico
* Almoço


---

## 🧠 2. Formulação do Problema

* **Tipo de aprendizado:** Aprendizado Supervisionado
* **Tarefa:** Classificação
* **Variável alvo (target):** Situação do aluno (Aprovado = 1, Reprovado = 0)

---

## 📥 3. Coleta de Dados

**Fonte dos dados**: [Kaggle - Student Performance](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
```


## 🧼 4. Pré-processamento

* Criação da variável `media`: média das três notas.
* Criação da variável `aprovado`: 1 se média ≥ 60, 0 caso contrário.
* Divisão do dataset em treino (70%) e teste (30%).

---

## 📊 5. Análise Exploratória

Foi observado: 
* Vários alunos não fazem curso preparatório.
* Almoço fraco pode prejudicar o desempenho.


---

## 🧪 6. Treinamento do Modelo

* Algoritmo usado: `RandomForestClassifier`
* Métricas de avaliação: acurácia, precisão, recall, f1-score, matriz de confusão

---

## 📈 7. Importância das Variáveis

A variável almoço demonstrou alta importância no modelo. Essa variável, embora aparentemente simples, pode refletir aspectos socioeconômicos mais amplos que afetam diretamente a aprendizagem.
Alunos com almoço gratuito ou reduzido apresentaram médias mais baixas, sugerindo uma possível relação entre desempenho escolar e a renda da família

---

## 📊 8. Avaliação – Matriz de Confusão

|                    | Previsto Aprovado | Previsto Reprovado |
| ------------------ | ----------------- | ------------------ |
| **Real Aprovado**  | 82                | 8                  |
| **Real Reprovado** | 6                 | 24                 |

### 🔍 Interpretação:

* **VP (82)**: Modelo acertou quem foi aprovado.
* **VN (24)**: Modelo acertou quem foi reprovado.
* **FP (6)**: Previu aprovação, mas foi reprovado.
* **FN (8)**: Previu reprovação, mas foi aprovado.


## 📌 9. Conclusão

Pode-se dizer que o modelo teve uma **boa performance** em prever aprovação escolar com base em informações socioeconômicas.
Almoço e o curso preparatório se mostraram os fatores mais relevantes e mostram o impacto da **desigualdade social na educação**.

A baixa influência da escolaridade dos pais levanta hipóteses interessantes e demonstra que **a percepção intuitiva nem sempre reflete a realidade dos dados**.


