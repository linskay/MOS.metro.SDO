# Аналитический модуль прогнозирования и оценки упущенных продаж KUDO®

## Описание проекта

KUDO® — российская торговая марка аэрозольных лакокрасочных материалов, монтажной пены, клеёв, герметиков и бытовой химии. Торговая марка KUDO® принадлежит группе компаний «Русские технические аэрозоли» — крупнейшему российскому производителю аэрозолей технического назначения.

У компании есть многолетние данные о выполненных заказах, а также данные о заказах, которые не получилось выполнить. Также доступны дополнительные таблицы со справочной информацией: база товаров, база клиентов и другие.

Цель проекта — разработать прототип (MVP), который поможет:
- Прогнозировать будущие продажи с учетом сезонности и внешних факторов.
- Рекомендовать клиентам новые товары на основе их поведения (покупок).

По результатам проекта должен быть представлен работающий прототип с возможностью визуализации:
- Очистки и консолидации данных (выполненные/неисполненные заказы).
- Расчета "потенциальных" продаж при наличии товаров.
- Прогноза продаж на определенный период (например, на квартал или год вперед).
- Аналитических отчетов по трендам (по артикулу, группе, клиентам и т.д.).

---

## Структура проекта

### 1. Подготовка данных
#### Задачи:
- **Задача 1.1:** Загрузка и первичный анализ данных  
  - Оценка качества данных (пропуски, дубликаты, аномалии).  
  - Структурирование данных из разных таблиц.  
  - Ответственные: Аналитики, Python-разработчики.

- **Задача 1.2:** Очистка данных  
  - Устранение пропущенных значений и аномалий.  
  - Консолидация данных о выполненных и неисполненных заказах.  
  - Ответственные: Аналитики, Python-разработчики.

- **Задача 1.3:** Создание признаков  
  - Добавление новых переменных (например, сезонность, категория клиента, исторические продажи по SKU).  
  - Ответственные: Аналитики, Python-разработчики.

---

### 2. Прогнозирование будущих продаж
#### Задачи:
- **Задача 2.1:** Разработка моделей прогнозирования  
  - Реализация классических статистических моделей (ARIMA, SARIMA).  
  - Реализация моделей машинного обучения (XGBoost, LightGBM, Prophet).  
  - Ответственные: Python-разработчики.

- **Задача 2.2:** Оценка точности моделей  
  - Сравнение метрик качества (MAE, RMSE, MAPE).  
  - Выбор оптимальной модели или гибридного подхода.  
  - Ответственные: Аналитики, Python-разработчики.

- **Задача 2.3:** Прогноз на заданный период  
  - Генерация прогнозов на квартал/год вперед для каждого SKU.  
  - Ответственные: Python-разработчики.

---

### 3. Оценка упущенных продаж
#### Задачи:
- **Задача 3.1:** Анализ неисполненных заказов  
  - Определение причин отказов (недостаток товара, неправильные запросы клиентов).  
  - Расчет потенциальных продаж для каждого случая.  
  - Ответственные: Аналитики, Python-разработчики.

- **Задача 3.2:** Подсчет экономической выгоды  
  - Оценка потенциальной прибыли от "упущенных" продаж.  
  - Ответственные: Аналитики.

---

### 4. Рекомендации товаров клиентам
#### Задачи:
- **Задача 4.1:** Разработка системы рекомендаций  
  - Использование алгоритмов коллаборативной фильтрации или контент-базированных методов.  
  - Ответственные: Python-разработчики.

- **Задача 4.2:** Тестирование рекомендаций  
  - Проверка релевантности рекомендаций на тестовых данных.  
  - Ответственные: Аналитики, Python-разработчики.

---

### 5. Визуализация и отчетность
#### Задачи:
- **Задача 5.1:** Создание интерактивных графиков  
  - Визуализация трендов по SKU, группам товаров, регионам.  
  - Ответственные: Аналитики, Python-разработчики.

- **Задача 5.2:** Разработка аналитического дашборда  
  - Интеграция всех ключевых метрик и графиков в единый интерфейс.  
  - Возможные инструменты: Tableau, Power BI, Dash, Streamlit.  
  - Ответственные: Аналитики, Python-разработчики.

---

### 6. Тестирование и оптимизация
#### Задачи:
- **Задача 6.1:** Проверка работоспособности прототипа  
  - Тестирование на различных наборах данных.  
  - Проверка времени выполнения расчетов.  
  - Ответственные: Тестировщики, Python-разработчики.

- **Задача 6.2:** Оптимизация производительности  
  - Ускорение обработки данных и расчетов.  
  - Ответственные: Python-разработчики.

---

### 7. Документация и презентация
#### Задачи:
- **Задача 7.1:** Подготовка документации  
  - Описание архитектуры решения.  
  - Объяснение выбора моделей и методов.  
  - Ответственные: Все роли.

- **Задача 7.2:** Создание презентации  
  - Краткое описание функционала и результатов.  
  - Демонстрация работы прототипа.  
  - Ответственные: Все роли.

---

## Ролевые обязанности

- **Аналитики:**
  - Анализ бизнес-требований.
  - Подготовка данных и создание признаков.
  - Оценка экономической выгоды.
  - Визуализация и отчетность.

- **Тестировщики:**
  - Проверка корректности работы модулей.
  - Выявление ошибок и багов.

- **Python-разработчики:**
  - Реализация моделей прогнозирования и рекомендаций.
  - Оптимизация кода и производительности.
  - Интеграция компонентов.

---

## Финальный продукт

- Прототип MVP с возможностью:
  - Прогнозировать продажи.
  - Оценивать упущенные продажи.
  - Рекомендовать товары клиентам.
- Интерактивный дашборд для визуализации данных.
- Документация и презентация решения.

---

## Технические требования

1. **Язык и стек технологий:** На усмотрение участников.
2. **Требования к производительности:**
   - Решение должно уметь работать с большими объемами данных (несколько лет истории, события, несколько тысяч SKU и клиентов).
   - Разумное время расчетов (до нескольких минут на финальных тестовых данных).
3. **Формат итоговой демонстрации:**
   - Прототип или ноутбук с документированным кодом.
   - Визуализация итоговых результатов (дашборд, интерактивная веб-страница, графики в Jupyter и т.п.).
   - Краткая презентация о том, как решение работает.
