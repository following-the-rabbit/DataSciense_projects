# Машинное обучение для текстов
# Поиск токсичных комментариев
### Описание проекта:
Интернет-магазин запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию.
### Описание данных:
Набор данных с разметкой о токсичности правок.
### Цели проекта: 
- Обучить модель классифицировать комментарии на позитивные и негативные. В распоряжении набор данных с разметкой о токсичности правок.
- Построить модель со значением метрики качества F1 не меньше 0.75.
### В ходе проекта выполнено:
- Предобработка Данных
    - Лемматизация с помощью WordNetLemmatizer библиотеки nltk
    - Удаление лишних символов
    - Удаление стоп-слов (список взят из библиотеки nltk)
   - Векторизация корпуса с помощью TfidfVectorizer
- Обучение моделей
    - Logistic Regression
    - NB-SVM
    - Linear SVC
- Анализ результатов предсказаний

### Вывод:
- На получившихся данных обучены модели, значение f1:
    -	LogisticRegression 0.775
    -	NB-SVM 0.788
    -	LinearSVC 0.775
- Качество моделей практически одинаково. Разница не более 1%. Максимальный показатель f1 получен для NB-SVM: 0.788
- Кросс-валидация моделей и подбор гиперпараметров проводились с помощью GridSearchCV.
- Проверка на адекватность была проведена для модели LogisticRegression.

### Используемый стек инструментов:
- python
- pandas
- numpy
- sklearn
- nltk
- seaborn