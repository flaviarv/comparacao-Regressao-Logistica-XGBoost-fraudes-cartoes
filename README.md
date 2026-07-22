TRABALHO COMPLETO: https://medium.com/@rv.flavia/4bd5070b7402

# Sumário Executivo

O objetivo desse trabalho é comparar a eficiência dos modelos de Regressão Logística e XGBoost para detectar fraudes em cartões de crédito.

Hospedada pelo TensorFlow, o dataset utilizado é “Credit Card Fraud Detection”, originalmente publicado no Kaggle pelo grupo de pesquisa MLG — Machine Learning Group da Université Libre de Bruxelles.

Este trabalho desenvolve e avalia modelos de Machine Learning para detecção de fraudes em transações com cartões de crédito, utilizando um conjunto de dados cujas variáveis originais foram anonimizadas por meio da técnica de Análise de Componentes Principais (PCA), preservando a confidencialidade das informações.

O primeiro desafio é o forte desbalanceamento da variável alvo, em que aproximadamente 99,82% das transações são legítimas e apenas 0,17% correspondem a fraudes.

Na etapa de preparação dos dados, a variável Amount passou por transformação logarítmica para reduzir a influência de outliers e, posteriormente, foi padronizada com StandardScaler, garantindo compatibilidade de escala com as demais variáveis.

Em seguida, o dataset foi dividido em 70% para treinamento e 30% para teste, utilizando amostragem estratificada (stratify) para preservar a proporção de fraudes em ambos os conjuntos.

O estudo comparou dois modelos de classificação: Regressão Logística e XGBoost. Para lidar com o desbalanceamento das classes, o XGBoost foi configurado com o parâmetro scale_pos_weight=10, aumentando a penalidade para erros em que uma fraude fosse classificada como transação legítima, tornando o modelo mais sensível à identificação de operações fraudulentas.

Os resultados demonstraram a superioridade do XGBoost em relação à Regressão Logística. O modelo elevou a Precision de 86% para 94%, o Recall de 64% para 78% e o F1-Score de 0,74 para 0,85, evidenciando maior capacidade de detectar fraudes sem aumentar significativamente os falsos positivos.

Em conclusão, o XGBoost apresentou um desempenho mais robusto e equilibrado para um cenário altamente desbalanceado, oferecendo maior eficiência na identificação de transações fraudulentas e maior confiabilidade para aplicações reais no setor financeiro.

## Agradecimentos

Gostaria de deixar um agradecimento especial à professora Isadora Ferrão. Excelente didática e muito conhecimento técnico! 
