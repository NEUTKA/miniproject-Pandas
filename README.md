# Минипроект: Знакомство с Pandas

## О проекте
А вот и мой первый минипроект!  
В них даются данные и ряд вопросов разной сложности.

В этом мини-проекте предстоит проанализировать данные о бронировании отелей. Ниже приведены задачи, которые необходимо выполнить, и описание данных.

## Задачи
1. **Импорт данных**  
   - Импортировать библиотеку pandas как `pd`.
   - Загрузить датасет `bookings.csv` с разделителем `;`.
   - Проверить размер таблицы, типы переменных и вывести первые 7 строк, чтобы ознакомиться с данными.
   
2. **Предобработка данных**  
   - Привести названия колонок к нижнему регистру и заменить пробелы на знак нижнего подчеркивания.

3. **Анализ данных**  
   - Определить страны с наибольшим числом успешных бронирований. Указать топ-5 стран.
   - Рассчитать среднее количество ночей для каждого типа отеля.
   - Узнать, сколько раз тип номера, полученного клиентом (`assigned_room_type`), отличается от забронированного (`reserved_room_type`).
   - Проанализировать даты запланированного прибытия:
     - Определить, в каком месяце чаще всего бронировали в 2016 году. Изменился ли самый популярный месяц в 2017 году?
     - Сгруппировать данные по годам и выяснить, на какой месяц чаще всего приходились отмены для отеля типа City Hotel.
   - Посмотрить числовые характеристики переменных `adults`, `children` и `babies`. Какая из них имеет наибольшее среднее значение?
   - Создать колонку `total_kids`, объединив `children` и `babies`, и рассчитать среднее значение переменной для каждого типа отеля.
   - Создать переменную `has_kids`, которая принимает значение `True`, если клиент указал хотя бы одного ребенка (`total_kids > 0`), иначе `False`.
   - Рассчитать churn rate (отношение ушедших пользователей к общему количеству клиентов) и указать, в какой группе показатель выше.

## Описание данных
Имеются следующие переменные:

- **Hotel** – тип отеля (City Hotel или Resort Hotel)  
- **Is canceled** – бронирование было отменено (1) или нет (0); успешные бронирования не отменены  
- **Lead time** – количество дней, прошедших между датой бронирования и датой прибытия  
- **Arrival full date** – полная дата прибытия  
- **Arrival date year** – год прибытия  
- **Arrival date month** – месяц прибытия  
- **Arrival date week number** – номер недели прибытия  
- **Arrival date day of month** – день прибытия  
- **Stays in weekend nights** – количество выходных (суббота и воскресенье), забронированных для проживания в отеле  
- **Stays in week nights** – количество будних дней (с понедельника по пятницу), забронированных для проживания в отеле  
- **Stays total nights** – общее число забронированных ночей  
- **Adults** – число взрослых  
- **Children** – число детей  
- **Babies** – число младенцев  
- **Meal** – выбранный тип питания  
- **Country** – страна происхождения клиента  
- **Reserved room type** – тип забронированного номера  
- **Assigned room type** – тип полученного номера (может отличаться от забронированного)  
- **Customer type** – тип бронирования  
- **Reservation status** – последний статус брони:
  - `Canceled` - отменено клиентом
  - `Check-Out` - клиент зарегистрировался, но уже покинул отель
  - `No-Show` - клиент не зарегистрировался и не сообщил об отмене  
- **Reservation status date** – дата обновления статуса

# Mini-Project: Getting Started with Pandas

## About the Project
Here’s my first mini-project!  
In these projects, you’re given data and a series of questions of varying difficulty.

In this mini-project, the goal is to analyze hotel booking data. Below are the tasks to be completed and the data description.

## Tasks
1. **Data Import**  
   - Import the pandas library as `pd`.
   - Load the dataset `bookings.csv` with the delimiter `;`.
   - Check the table size, data types, and display the first 7 rows to get familiar with the data.
   
2. **Data Preprocessing**  
   - Convert column names to lowercase and replace spaces with underscores.

3. **Data Analysis**  
   - Identify the countries with the highest number of successful bookings. Specify the top 5 countries.
   - Calculate the average number of nights for each type of hotel.
   - Find out how many times the assigned room type (`assigned_room_type`) differed from the reserved room type (`reserved_room_type`).
   - Analyze planned arrival dates:
     - Determine the most popular booking month in 2016. Did the most popular month change in 2017?
     - Group the data by year and find out in which month cancellations were highest for City Hotel.
   - Examine the numerical characteristics of the variables `adults`, `children`, and `babies`. Which has the highest mean value?
   - Create a column `total_kids` by combining `children` and `babies`, and calculate the mean value of this variable for each hotel type.
   - Create a variable `has_kids` that takes the value `True` if a client has at least one child (`total_kids > 0`), otherwise `False`.
   - Calculate the churn rate (the ratio of departed users to total clients) and identify which group has a higher rate.

## Data Description
The dataset includes the following variables:

- **Hotel** – type of hotel (City Hotel or Resort Hotel)  
- **Is canceled** – whether the booking was canceled (1) or not (0); successful bookings were not canceled  
- **Lead time** – number of days between the booking date and the arrival date  
- **Arrival full date** – full arrival date  
- **Arrival date year** – arrival year  
- **Arrival date month** – arrival month  
- **Arrival date week number** – arrival week number  
- **Arrival date day of month** – arrival day of the month  
- **Stays in weekend nights** – number of weekend nights (Saturday and Sunday) booked at the hotel  
- **Stays in week nights** – number of weeknights (Monday through Friday) booked at the hotel  
- **Stays total nights** – total number of nights booked  
- **Adults** – number of adults  
- **Children** – number of children  
- **Babies** – number of infants  
- **Meal** – selected meal type  
- **Country** – client’s country of origin  
- **Reserved room type** – reserved room type  
- **Assigned room type** – assigned room type (may differ from the reserved type)  
- **Customer type** – type of booking  
- **Reservation status** – last booking status:
  - `Canceled` - canceled by the client
  - `Check-Out` - client checked in but has already left
  - `No-Show` - client didn’t check in and didn’t notify about the cancellation  
- **Reservation status date** – date the status was updated

