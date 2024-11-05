`scikit-learn` (или `sklearn`) — это библиотека машинного обучения для языка программирования [[Python]]. Она предоставляет простой и эффективный инструментарий для решения задач машинного обучения, таких как классификация, регрессия, кластеризация, уменьшение размерности, выбор модели и предварительная обработка данных. Библиотека построена на основе [[NumPy]], SciPy и [[Matplotlib]], что делает её очень удобной для использования в научных и инженерных приложениях.

### Основные компоненты `scikit-learn`

1. **Классификация (Classification)**:
    
    - **Модели**: `LogisticRegression`, `KNeighborsClassifier`, `DecisionTreeClassifier`, `RandomForestClassifier`, `SVM`, `GaussianNB`, и другие.
        
    - **Пример**: Предсказание категории (класса) на основе входных данных.
        
2. **Регрессия (Regression)**:
    
    - **Модели**: [[LinearRegression]], `Ridge`, `Lasso`, `ElasticNet`, `DecisionTreeRegressor`, `RandomForestRegressor`, и другие.
        
    - **Пример**: Предсказание непрерывных значений, таких как цена на недвижимость.
        
3. **Кластеризация (Clustering)**:
    
    - **Модели**: `KMeans`, `DBSCAN`, `AgglomerativeClustering`, `MeanShift`, и другие.
        
    - **Пример**: Группировка данных на основе сходства без предварительного знания о группах.
        
4. **Уменьшение размерности (Dimensionality Reduction)**:
    
    - **Модели**: `PCA` (Principal Component Analysis), `TSNE` (t-Distributed Stochastic Neighbor Embedding), `LDA` (Linear Discriminant Analysis), и другие.
        
    - **Пример**: Уменьшение количества признаков для упрощения модели и улучшения производительности.
        
5. **Выбор модели (Model Selection)**:
    
    - **Инструменты**: `GridSearchCV`, `RandomizedSearchCV`, `cross_val_score`, [[train_test_split]].
        
    - **Пример**: Оптимизация гиперпараметров модели и оценка её производительности.
        
6. **Предварительная обработка данных (Data Preprocessing)**:
    
    - **Инструменты**: `StandardScaler`, `MinMaxScaler`, `OneHotEncoder`, `LabelEncoder`, `PolynomialFeatures`, и другие.
        
    - **Пример**: Нормализация данных, кодирование категориальных признаков, создание полиномиальных признаков.