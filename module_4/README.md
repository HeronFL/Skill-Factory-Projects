# Skill-Factory-Projects
# Курс Skillfactory: DST-PRO. Профессия Data Scientist. Поток 5.

  
## Итоговое задание по Проекту 4. Авиарейсы без потерь (RDS).  
(Юнит 5. Работа с базами данных)  

## Оглавление  
[1. Основные цели и задачи проекта](https://github.com/HeronFL/Skill-Factory-Projects/blob/master/module_4/README.md#Основные-цели-и-задачи-проекта)  
[2.  Краткая информация о данных](https://github.com/HeronFL/Skill-Factory-Projects/blob/master/module_4/README.md#Краткая-информация-о-данных)  
[3. Этапы работы над проектом](https://github.com/HeronFL/Skill-Factory-Projects/blob/master/module_4/README.md#Этапы-работы-над-проектом)  
[4. Результат](https://github.com/HeronFL/Skill-Factory-Projects/blob/master/module_4/README.md#Результат)  

### Основные цели и задачи проекта  
Основные цели и задачи проекта: Отобрать необходимую информацию для анализа о невыгодных перелетах из Анапы в зимнее время на основе демонстрационной базы данных авиаперевозок по России. 

### Краткая информация о данных
В качестве предметной области дана демонстрационная база данных авиаперевозок по России. База данных состоит из восьми таблиц. Основной сущностью является бронирование (bookings).

В одно бронирование можно включить несколько пассажиров, каждому из которых выписывается отдельный билет (tickets). Билет имеет уникальный номер и содержит информацию о пассажире. Как таковой пассажир не является отдельной сущностью. Как имя, так и номер документа пассажира могут меняться с течением времени, так что невозможно однозначно найти все билеты одного человека; для простоты можно считать, что все пассажиры уникальны.

Билет включает один или несколько перелетов (ticket_flights). Несколько перелетов могут включаться в билет в случаях, когда нет прямого рейса, соединяющего пункты отправления и назначения (полет с пересадками), либо когда билет взят «туда и обратно». В схеме данных нет жёсткого ограничения, но предполагается, что все билеты в одном бронировании имеют одинаковый набор перелетов.

Каждый рейс (flights) следует из одного аэропорта (airports) в другой. Рейсы с одним номером имеют одинаковые пункты вылета и назначения, но будут отличаться датой отправления.

При регистрации на рейс пассажиру выдаётся посадочный талон (boarding_passes), в котором указано место в самолете. Пассажир может зарегистрироваться только на тот рейс, который есть у него в билете. Комбинация рейса и места в самолете должна быть уникальной, чтобы не допустить выдачу двух посадочных талонов на одно место.

Количество мест (seats) в самолете и их распределение по классам обслуживания зависит от модели самолета (aircrafts), выполняющего рейс. Предполагается, что каждая модель самолета имеет только одну компоновку салона. Схема данных не контролирует, что места в посадочных талонах соответствуют имеющимся в самолете (такая проверка может быть сделана с использованием табличных триггеров или в приложении).

### Этапы работы над проектом  
- знакомство с базой данных;  
- изучение закономерностей в данных;
- предварительный анализ;  
- формирование кода решения и датасета;
- презентация.  

### Результат  

Результат работы включает подготовленный датасет со структурой:
1.	flight_id — идентификатор рейса
2.	flight_no — номер рейса
3.	city_departure — город вылета Анапа
4.	city_arrival — город прибытия
5.	timezone — часовой пояс аэропорта прибытия
6.	latitude— долгота аэропорта прибытия
7.	longitude — широта аэропорта прибытия
8.	model — модель самолета
9.	range — максимальная дальность полета самолета в км
10.	scheduled_departure — дата и время вылета по расписанию
11.	scheduled_arrival — дата и время прибытия по расписанию
12.	actual_departure — фактическое время вылета
13.	actual_arrival — фактическое время прибытия
14.	departure_airport — аэропорт отправления
15.	arrival_airport — аэропорт прибытия
16.	aircraft_code — код самолета
17.	way_minutes — время полета в рейсе
18.	count_seats — количество мест в самолете
19.	count_ticket — количество проданных билетов всего на рейс
20.	occupancy - процент заполненности рейса 
21.	sum_amout — сумма проданных билетов на рейс
22.	count_economy — количество проданных билетов эконом класса
23.	sum_econom — сумма проданных билетов эконом класса
24.	count_business — количество проданных билетов бизнес класса
25.	sum_business — сумма проданных билетов бизнес класса


