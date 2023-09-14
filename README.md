# Домашнее задание к занятию "`Базы данных, их типы`" - `Стрекозов Владимир`
### Задание 1
Кейс

Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

**Ответ:**   
Реляционная СУБД. В таких решениях СУБД работает с небольшими по размерам транзакциями, но идущими большим потоком, и при этом от системы требуется минимальное время отклика, а так же возможность, при определенных условиях, отменить любые изменения выполняемых в рамках транзакции.

1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы?

**Ответ:**   
Полагаю что речь идёи об API облачного провайдера, например yandex cloud с managed DB

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

**Ответ:**   
Так же можно использовать реляционную СУБД. Т.к. данный тип СУБД успешно работает с данными, которые буду генерироваться в проектах.

1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?

**Ответ:**   
На сколько знаю для сайтов часто используют MySQL.

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

**Ответ:**   
По идее можно так же использовать реляционную СУБД.

1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это реализовать?

**Ответ:**   
Полагаю что речь идео о своего рода корпоративного wiki, то можно использовать тот же mySQL, в которой можно хранить и документы и текст и пр.

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

**Ответ:**   
Так же предлагаю реляционную СУБД. Т.к. необходимо будет хранить информацию разного типа, так же необходимы будут связи между таблицами.

1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД логистов?

**Ответ:**   
Можно подключить, только создать свой набор таблиц и связей.

1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?

**Ответ:**   
Исходя из моих ответов - можно. Тот же postgres можно использовать под задачи, описанные выше.

Приведите ответ в свободной форме.
---

### Задание 2
Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.

**Ответ:**   
 1.Запрашиваем сумму пополнения
 2. Проверяем что денег на счете достаточно
 3. Уменьшаем сумму на счете на сумму пополнения
 4. Запрашиваем текущий баланс
 5.Увеличиваем текущий баланс на сумму
 6. Проверяем что баланс увеличился
 
2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?

**Ответ:**   
 1. Проверяем признак автоплатежа
 2. Проверяем дату автоплатежа
 3. Проверяем текущую дату
 4. Запрашиваем сумму пополнения
 5. Проверяем что денег на счете достаточно
 6. Уменьшаем сумму на счете на сумму пополнения
 7. Запрашиваем текущий баланс
 8. Увеличиваем текущий баланс на сумму
 9. Проверяем что баланс увеличился
Приведите ответ в свободной форме.**
---

### Задание 3
SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.

**Ответ:**

3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

**Ответ:**

Приведите ответ в свободной форме.

### Задание 4
Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.

**Ответ:**

На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

Приведите ответ в свободной форме.
