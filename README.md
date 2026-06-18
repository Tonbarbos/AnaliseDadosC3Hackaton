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
[INSERIR AQUI O QUE FALTA NA PARTE DO DANTON]
 
## Tecnologias utilizadas
 
- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Scikit-learn
- MLxtend (Apriori)
- Jupyter Notebook
