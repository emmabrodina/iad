# Проект: Класифікація сегментації клієнтів автосалону

Цей проект включає виконання завдань з класифікації, де використовувалися різні алгоритми машинного навчання для аналізу даних про сегментацію клієнтів в автомобільному салоні. Нижче наведено основні етапи виконаної роботи.

## Етапи роботи

1. **Завантаження даних**
   - Завантажено початковий набір даних та виведено назви колонок і розмір датасету.

2. **Опрацювання пропусків**
   - Пропущені значення оброблено: заповнено відповідними значеннями або видалено, якщо це було доцільно.

3. **Візуалізація даних**
   - Побудовано графік кореляцій (heatmap), що відображає взаємозв'язок ознак між собою та з цільовою змінною.
   - Побудовано гістограми розподілу ознак та boxplot-и ознак відносно цільової змінної. У випадку великої кількості ознак візуалізація виконувалася для основних характеристик.

4. **Нормалізація даних**
   - Здійснено нормалізацію ознак для підвищення ефективності навчання моделей.

5. **Навчання моделей**
   - Виконано навчання наступних класифікаторів:
     - `k-Nearest Neighbors (kNN)`
     - `Decision Tree (дерево ухвалення рішень)`
     - `Support Vector Machine (SVM)`
     - `Random Forest`
     - `AdaBoost`
   - Для кожного алгоритму підібрано оптимальні параметри:
     - Для `kNN` підібрано найкращу кількість сусідів.
     - Для `SVM` використано `GridSearchCV` для підбору оптимальних значень параметрів `C` і `gamma`.

6. **Оцінка та вибір найкращої моделі**
   - Серед обраних оптимальних моделей кожного алгоритму було вибрано найкращу на основі результатів точності її роботи.
   - Відображено звіт `classification_report` та матрицю плутанини `confusion_matrix` для кожної моделі.

## Структура проекту

- `solved_task` — папка з виконаними завданнями (код, моделі, візуалізації).
- `customer-segmentation-classification` — початковий набір даних.
- `processed_data` — дані після обробки пропущених значень і виключення викидів.
- `processed_data_encoding` — дані після кодування категоріальних змінних і нормалізації числових змінних (основний набір для подальшого моделювання)

## Використані технології

- Мова програмування: `Python`
- Бібліотеки: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

## Як запустити проект

1. Клонувати репозиторій:
   ```bash
   git clone <посилання на репозиторій>

2. Перейти до папки проекту: 
   cd <назва проекту>

3. Запустити файл solved_task.ipynb з папки lab1 для виконання основного аналізу.
