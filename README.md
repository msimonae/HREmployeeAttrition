# HREmployeeAttrition
Employee Analysis | Attrition Report Predict attrition of your valuable employees

Resumo da Estrutura do Notebook1. 
1.Pré-processamento Anti-Leakage: Uso rigoroso de ColumnTransformer e Pipeline para o processo de limpeza (Imputação, Escalonamento Z-Score, OneHotEncoder) sem usar dados do conjunto de Teste.
2. Abordagens Filter e Wrapper: Utilizamos k=10 para as comparações. Aplicamos o SelectKBest e mutual_info_classif para capturar a relação univariada, enquanto o RFE foi encarregado da extração recursiva baseada no modelo.
3. SHAP e XAI: Construímos um explicador TreeExplainer no modelo base, geramos o Summary Plot visual, e extraímos as 10 variáveis globais com o maior impacto (valor absoluto) na predição de Attrition.  
4 e 5. Modelo e Avaliação Comparativa: Um modelo RandomForestClassifier otimizado foi iterado 4 vezes (Base Completa, Filter, Wrapper, SHAP). As métricas de Accuracy, Precision, Recall e F1-Score são retornadas de forma tabulada para justificar o melhor classificador.  
Discussão: A última célula calcula a intersecção de conjuntos, listando os atributos que foram unânimes entre as técnicas e quais foram exclusivos.
