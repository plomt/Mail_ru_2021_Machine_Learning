**Problem 1.**
***
В качестве домашнего задания вам предлагается поработать над предсказанием погоды в Австралии. Файл с данными вы найдете в соответствующей директории. Вам будет доступен датасет weatherAUS.csv, ПЕРВЫЕ 75% (shuffle = False) которого нужно взять для обучения, последние 25% - для тестирования.

Требуется построить 3 модели которые будут предсказывать целевую переменную RainTomorrow:

1. С помощью Байесовских классификаторов
2. С помощью логистической регрессии
3. С помощью метода ближайших соседей

Затем следует сравнить результаты моделей (по качеству и времени выполнения) и сделать вывод о том, какая модель и с какими параметрами даёт лучшие результаты. В конце ноутбука должны быть четко описаны полученные результаты и метрики.

Не забывайте о том, что работа с признаками играет очень большую роль в построении хорошей модели.

Краткое описание данных:

1. Date - Дата наблюдений
2. Location - Название локации, в которой расположена метеорологическая станция
3. MinTemp - Минимальная температура в градусах цельсия
4. MaxTemp - Максимальная температура в градусах цельсия
5. Rainfall - Количество осадков, зафиксированных за день в мм
6. Evaporation - Так называемое "pan evaporation" класса А (мм) за 24 часа до 9 утра
7. Sunshine - Число солнечных часов за день
8. WindGustDir - направление самого сильного порыва ветра за последние 24 часа
9. WindGustSpeed - скорость (км / ч) самого сильного порыва ветра за последние 24 часа
10. WindDir9am - направление ветра в 9 утра

**Problem 2.**
***
**Постановка задачи:**
Необходимо реализовать функции accuracy_score, precision_score, recall_score, lift_score, f1_score (названия функций должны совпадать). Каждая функция должна иметь 3 обязательных параметра def precision_score(y_true, y_predict, percent=None). Добавлять свои параметры нельзя.

1. Нельзя использовать готовые реализации этих метрик
2. Если percent=None то метрика должна быть рассчитана по порогу вероятности >=0.5
3. Если параметр percent принимает значения от 1 до 100 то метрика должна быть рассчитана на соответствующем ТОПе
4. 1 - верхний 1% выборки
5. 100 - вся выборка
6. y_predict - имеет размерность (N_rows; N_classes)