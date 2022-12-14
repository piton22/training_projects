## Описание проекта

Сетевой супермаркет внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:

Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы;
Контролировать добросовестность кассиров при продаже алкоголя.
Необходимо построить модель, которая приблизительно определит возраст покупателя. В распоряжении набор фотографий людей с указанием возраста.

## Статус проекта
Завершен

## Сфера деятельности
Бизнес, оффлайн

## Данные 
* фото лиц в формате jpeg
* возраст

## Задачи
1. Провести исследовательский анализ набора фотографий.
2. Подготовить данные к обучению.
3. Обучить нейронную сеть и рассчитать её качество.

## Выводы

По итогу проекта обучили нейросеть архитектуры ResNet50, в качестве финального слоя выбрали полносвязный слой с 1 нейроном и ReLu - активацией. Использовали предобученные веса ImageNet. Обучение модели проводили при следующих параметрах: размер батча 32, оптимизатор Adam со скоростью обучения 0.0001, 10 эпох, без заморозки весов. Среднее абсолютное отклонение на обучающей выборке получили 2.1414, на тестовой 6.0136. Т.к. качество предсказаний отличается почти в 3 раза, модель переобучена. Однако достигнутое качество соответствует требованиям.

## Используемые библиотеки
*pandas, matplotlib, keras*
