# Análise de Preços de Casas nos EUA
O objetivo é explorar o dataset de preços de casas nos EUA e aplicar técnicas de análise exploratória, engenharia de features, aprendizagem supervisionada e não supervisionada.
 
 
## Integrantes do Grupo

- **[Ana Luiza Menelli Taylor](https://github.com/analuizataylor)**
- **[Danton Barbosa](https://github.com/Tonbarbos)**
- **[Felipe Valério Rocha](https://github.com/felipevaleriorocha)**
- **[Karoliny Franco](https://github.com/karolinyfranco)**
- **[Gustavo Rissoli](https://github.com/Gustavo-Rissoli)**
 
 
### 1. Análise Exploratória de Dados
- Identificação de variáveis numéricas e categóricas
- Análise de valores faltantes
- Detecção de outliers via método IQR com boxplots
- Matriz de correlação

### 2. Feature Engineering
- Tratamento de valores faltantes (mediana para numéricas, moda para categóricas)
- Criação de novas features
- Codificação de variáveis categóricas
- Seleção de variáveis com correlação ≥ 0.3 com o target
  
### 3. Aprendizagem Supervisionada
**Regressão Linear** — prever o preço de venda:
- Diferença RMSE/MAE indica presença de outliers com erros elevados
  
**Regressão Logística** — classificar preço como alto ou baixo:
- Variável binária criada a partir da mediana do preço
- Avaliação com matriz de confusão e classification report
### 4. Aprendizagem Não Supervisionada
 
**Clusterização + Redução de Dimensionalidade**
- PCA com componentes para visualização
- KMeans escolhido pelo Método do Cotovelo
- Silhouette Score calculado para validar a qualidade dos clusters
- Perfil médio de cada cluster analisado

**Análise de Associação**
- Algoritmo Apriori com suporte mínimo de 20% e confiança mínima de 60%
- Regras com lift e associações reais entre características
- Padrões encontrados
  
**Detecção de Outliers**
- Local Outlier Factor (LOF)
- Resultado consistente com a análise de resíduos da regressão linear
  
### 5. Métricas de Avaliação e Comparação

Consolidação de todos os modelos em um só lugar, reavaliados sobre o mesmo
dataset processado e o mesmo split de treino/teste (random_state=42), para
garantir uma comparação justa entre eles.

**Glossário das métricas**
* Regressão: RMSE, MAE e R²
* Classificação: Acurácia, Precisão, Recall, F1 e ROC-AUC

**Comparação dos modelos de Regressão**
* Seis modelos avaliados: Regressão Linear, Ridge, Lasso, Árvore de Decisão,
  Random Forest e Gradient Boosting
* Regressão Linear explica ~81% da variação do preço (R² ≈ 0.81)
* Gradient Boosting foi o melhor (R² ≈ 0.91, erro médio de ~US$ 16 mil), por
  captar relações não lineares
* Gráficos comparativos (R², RMSE, MAE) e gráfico Previsto × Real do melhor modelo

**Comparação dos modelos de Classificação**
* Cinco classificadores avaliados: Regressão Logística, KNN, Árvore de Decisão,
  Random Forest e Gradient Boosting
* Todos acima de 89% de acurácia, com F1 ≈ 0.92 e ROC-AUC ≈ 0.98 no melhor caso
* Curvas ROC de todos os modelos e matriz de confusão do melhor classificador

**Comparação geral: supervisionado × não supervisionado**
* Tabela comparando objetivo, forma de avaliação e resultados de cada abordagem
* O não supervisionado descobriu a estrutura do mercado e o supervisionado
  confirmou e quantificou essa estrutura prevendo o preço

**Conclusão**
* Trade-off entre interpretabilidade (modelos lineares) e precisão (modelos de árvore)
* Recomendação de uso de cada modelo e limitações do projeto
 
## Tecnologias utilizadas
 
- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Scikit-learn
- MLxtend (Apriori)
- Jupyter Notebook
