# Определение стоимости автомобилей

## Предполагаемый заказчик

Сервис по продаже автомобилей с пробегом

## Цель проекта

Проект по машинному обучению. На основе исторических данных: технических характеристик, комплектации и цены автомобилей, построить модель для определения рыночной стоимости автомобиля. Заказчику важны качество предсказания, скорость предсказания и время обучения

## Общие выводы

Перед нами стояла задача разработки модели по определению рыночной стоимости автомобиля для сервиса по продаже автомобилей с пробегом. Для этого нам были предоставлены исторические данные: технические характеристики, комплектации и цены автомобилей.

На первом этапе был обработан датасет с историческими данными технических характеристик, комплектации и цены автомобилей. Были удалены дубликаты, аномальные значения года регистрации автомобилей и мощности двигателей. Так же были удалены строки с пропусками в столбце модели автомобиля. Пропуски в столбцах типа кузова, коробки передач и типа топлива были заполнены наиболее часто встреающимся значением для каждой марки и модели машины. В столбец 'repaired' была добавлена новая переменная 'undefined' взамен пропущенных значений. В общей сумме было удалено почти 20% данных.

На следующем этапе были обучены три модели и подоюраны оптимальные гиперпараметры для них. Для обучения были выбраны модели Random Forest, и модели градиентного бустинга из библиотек LightGBM и CatBoost.

На третьем этапе мы сравнили модели с точки зрения времени обучения и предсказания. Для сравнения использовали подобранные ранее гиперпараметры моделей, а так же подобранные модели градиентного бустинга с увеличенным числом итераций. Учитывая пожелания заказчика к качеству предсказания, времени обучения модели и предсказания была выбрана модель LightGBM с числом итераций равным 400.

Проверка выбранной модели на тестовой выборке показала метрику RMSE равную 1515.

## Инструменты

`Python`, `Pandas` , `Scikit-learn` , `Matplotlib` , `Seaborn`, `LightGBM`, `CatBoost`

## Ключевые слова проекта

`градиентный бустинг`, `регрессия`
