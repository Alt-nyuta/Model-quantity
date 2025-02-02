Описание исследования

Интернет-магазин "В один клик" продает разные товары: для детей, для дома, мелкую бытовую технику, косметику и продукты. По данным отчетов активность покупателей магазина начинается снижаться. Привлекать новых клиентов малоэффективно, так как с большей частью целевой аудитории работа уже была проведена. Выход их ситуации - поддержание активности постоянных клиентов за счет персонализированных предложений.

В связи с этим необходимо разработать решение, которое позволит персонализировать предложения постоянным клиентам для увеличения покупательской активности.

Цель исследования

Построить модель, которая предскажет веряотность снижения покупательской активности клиента в следующие три месяца;
Выделить сегменты покупателей и разработать для них персонализированные предложения.
Задачи исследования

- - Загрузить данные и проверить их на соответствие описанию

- - Предобработать данные

- - Провести исследовательский анализ данных

- - Объединить таблицы

Объедините таблицы market_file.csv, market_money.csv, market_time.csv.
Учесть, что данные о выручке и времени на сайте находятся в одном столбце для всех периодов. В итоговой таблице сделать отдельный столбец для каждого периода.
- - Провести корреляционный анализ

- - Подготовить пайплайн для подготовки данных и построения моделей классификации

Во время подготовки данных использовать ColumnTransformer. Количественные и категориальные признаки обработать в пайплайне раздельно. Для кодирования категориальных признаков использовать как минимум два кодировщика, для масштабирования количественных — как минимум два скейлера.
- - Обучить четыре модели: KNeighborsClassifier(), DecisionTreeClassifier(), LogisticRegression() и SVC().
Выбрать лучшую модель, используя заданную метрику с применением следующей стратегии - использовать один общий пайплайн для всех моделей и инструмент подбора гиперпараметров, который вернёт вам лучшую модель.
- - Провести анализ важности признаков

- - Оценить важность признаков для лучшей модели и постройте график важности с помощью метода SHAP
- - Сделать выводы о значимости признаков:
какие признаки мало значимы для модели;
какие признаки сильнее всего влияют на целевой признак;
как можно использовать эти наблюдения при моделировании и принятии бизнес-решений.
Провести сегментацию покупателей

- - Выполнить сегментацию покупателей.
Предложить, как увеличить покупательскую активность выбранного сегмента:
Провести графическое и аналитическое исследование группы покупателей.
Сделать предложения по работе с сегментом для увеличения покупательской активности.
Подготовить общие выводы по итогам исследования.

Исходные данные

market_file.csv - таблица, содержащая данные о поведении покупателя на сайте, о коммуникациях с покупателем и его продуктовом поведении.

id — номер покупателя в корпоративной базе данных.

Покупательская активность — рассчитанный класс покупательской активности (целевой признак): «снизилась» или «прежний уровень».

Тип сервиса — уровень сервиса, например «премиум» и «стандарт».

Разрешить сообщать — информация о том, можно ли присылать покупателю дополнительные предложения о товаре. Согласие на это даёт покупатель.

Маркет_актив_6_мес — среднемесячное значение маркетинговых коммуникаций компании, которое приходилось на покупателя за последние 6 месяцев. Это значение показывает, какое число рассылок, звонков, показов рекламы и прочего приходилось на клиента.

Маркет_актив_тек_мес — количество маркетинговых коммуникаций в текущем месяце.

Длительность — значение, которое показывает, сколько дней прошло с момента регистрации покупателя на сайте.

Акционные_покупки — среднемесячная доля покупок по акции от общего числа покупок за последние 6 месяцев.

Популярная_категория — самая популярная категория товаров у покупателя за последние 6 месяцев.

Средний_просмотр_категорий_за_визит — показывает, сколько в среднем категорий покупатель просмотрел за визит в течение последнего месяца.

Неоплаченные_продукты_штук_квартал — общее число неоплаченных товаров в корзине за последние 3 месяца.

Ошибка_сервиса — число сбоев, которые коснулись покупателя во время посещения сайта.

Страниц_за_визит — среднее количество страниц, которые просмотрел покупатель за один визит на сайт за последние 3 месяца.

market_money.csv - таблица с данными о выручке, которую получает магазин с покупателя, то есть сколько покупатель всего потратил за период взаимодействия с сайтом.

id — номер покупателя в корпоративной базе данных.

Период — название периода, во время которого зафиксирована выручка. Например, 'текущий_месяц' или 'предыдущий_месяц'.

Выручка — сумма выручки за период.

market_time.csv - таблица с данными о времени (в минутах), которое покупатель провёл на сайте в течение периода.

id — номер покупателя в корпоративной базе данных.

Период — название периода, во время которого зафиксировано общее время. минут — значение времени, проведённого на сайте, в минутах.

money.csv - таблица с данными о среднемесячной прибыли покупателя за последние 3 месяца: какую прибыль получает магазин от продаж каждому покупателю.

id — номер покупателя в корпоративной базе данных.

Прибыль — значение прибыли.
