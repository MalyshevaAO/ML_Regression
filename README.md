# 🎯 Реализация градиентного спуска для линейной регрессии

Этот проект демонстрирует реализацию градиентного спуска для обучения модели линейной регрессии с минимазацией среднеквадратичной ошибки (MSE).

## 📌 Описание

Проект включает:
- Реализацию класса `GradientDescentMse` для градиентного спуска
- Сравнение с линейной регрессией из `sklearn`
- Визуализацию процесса обучения для разных гиперпараметров

## 🔑 Ключевые компоненты

### Класс `GradientDescentMse`
Содержит методы для:
- Добавления константного признака (`add_constant_feature`)
- Расчёта MSE (`calculate_mse_loss`)
- Вычисления градиента (`calculate_gradient`)
- Итеративного обучения (`iteration` и `learn`)

### Гиперпараметры
- `learning_rate`: шаг градиентного спуска (по умолчанию 1e-3)
- `threshold`: критерий остановки (по умолчанию 1e-6)
- `copy`: флаг копирования данных

## 📊 Результаты

Проект включает визуализацию процесса обучения для различных комбинаций:
- 4 значения threshold (1e-2, 1e-3, 1e-4, 1e-5)
- 5 значений learning rate (1e-1, 5e-2, 1e-2, 5e-3, 1e-3)

Графики показывают сходимость алгоритма и итоговое значение функции потерь для каждой комбинации параметров.

## 🚀 Использование
1. Загрузите данные в формате CSV
2. Инициализируйте класс `GradientDescentMse`
3. Добавьте константный признак (`add_constant_feature`)
4. Запустите обучение (`learn`)
5. Визуализируйте результаты

Пример:
```python
GD = GradientDescentMse(samples=X, targets=Y, threshold=1e-5, learning_rate=1e-2)
GD.add_constant_feature()
GD.learn()
print(GD.betas)
