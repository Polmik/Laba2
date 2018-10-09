# Требования к проекту
---

# Содержание
1 [Введение](#intro)  
1.1 [Назначение](#appointment)  
1.2 [Бизнес-требования](#business_requirements)  
1.2.1 [Возможности бизнеса](#business_opportunities)  
2 [Требования пользователя](#user_requirements)  
2.1 [Программные интерфейсы](#software_interfaces)  
2.2 [Интерфейс пользователя](#user_interface)  
2.3 [Характеристики пользователей](#user_specifications)  
2.4 [Предположения и зависимости](#assumptions_and_dependencies)  
3 [Системные требования](#system_requirements)  
3.1 [Функциональные требования](#functional_requirements)  
3.2 [Нефункциональные требования](#non-functional_requirements)  
3.2.1 [Атрибуты качества](#quality_attributes)  
3.2.2 [Требования к безопасности](#security_requirements)  

<a name="intro"/>

# 1 Введение

Тип приложения: Насыщенное клиентское Desktop-приложение.  
Название продукта: Сервис – Склад.

<a name="appointment"/>

## 1.1 Назначение
Фиксирование доступного товара и сделанных заказов в интернет-магазине.  
Продукт должен обеспечивать:  
1) Обработку данных о доступных товарах в интернет-магазине (добавление, изменение, хранение, поиск, удаление).  
2) Обработку данных о сделанных заказах в интернет-магазине (добавление, изменение, хранение, поиск, удаление).

<a name="business_requirements"/>

## 1.2 Бизнес-требования

<a name="business_opportunities"/>
### 1.2.1 Исходные данные
Внедрение сервис–склада позволит сократить время поиска необходимого товара, сократить время оформления заказа, что повысит эффективность работы склада.

<a name="user_requirements"/>

# 2 Требования пользователя

<a name="software_interfaces"/>

## 2.1 Программные интерфейсы

1. Графический интерфейс пользователя должен обеспечиваться встроенными в Windows системными библиотеками Windows API.
2. Список товаров, заказов, а также данные о них хранятся с использованием системы управления базами данных (СУБД) – MySQL;

<a name="user_interface"/>

## 2.2 Интерфейс пользователя
 
![Главное окно программы](/Images/MainForm.png)  
Рисунок 1. Главное окно программы

Главное окно программы (рисунок 1) должно содержать два дочерних окна:  
1. окно в левой части для отображения списка товаров,  
2. окно в правой части для отображения списка заказов.  

Дочерние окна должны иметь вертикальные полосы прокрутки с правой стороны.  

Дочернее окно со списком товаров должно разделяться на колонки:  
1. Код товара (целое положительное число),  
2. Категория (строка),  
3. Название (строка),  
4. Цена (дробное положительное число с двумя цифрами после запятой),  
5. Количество (три целых положительных числа):  
- доступный товар,  
- самовывоз,  
- доставка.

Дочернее окно со списком заказов должно разделяться на колонки:  
1. № заказа (целое положительное число),  
2. Статус (строка),  
3. Информация (строка):  
- товар, его количество и стоимость,  
- ФИО заказчика,  
- номер телефона и провайдер,  
- адрес доставки,  
- заметки.

Главное меню приложения должно содержать меню «Файл» включающее пункты-подменю, соответствующие контекстным меню дочерних окон "Товары" и "Заказы"

Контекстное меню дочернего окна со списком товаров должно включать следующие пункты-команды:  
Поиск…		- Поиск товара в списке товаров.  
Добавить…	- Добавление в список товаров нового товара.  
Изменить…	- Изменение данных выбранного товара.  
Удалить…	- Удаление из списка товаров выбранного товара.  
Заказ…		- Добавление в список заказов нового заказа на выбранный товар.

Контекстное меню дочернего окна со списком заказов должно включать следующие пункты-команды:  
Поиск…		- Поиск заказа в списке заказов.  
Изменить…	- Изменение данных выбранного заказа.  
Вручено		- Удаление из списка заказов выбранного заказа.  
Возврат		- Отмена заказа.

<a name="user_specifications"/>

## 2.3 Характеристики пользователей
Пользователи продукта подразделяются на:  
1. Сотрудники, регистрирующие товары, поступившие на склад интернет-магазина.  
2. Сотрудники, принимающие заказы.  
Указанные пользователи составляют один класс: обычные пользователи, которые в состоянии работать с интуитивно-понятной, лёгкой для освоения системой.

<a name="assumptions_and_dependencies"/>

## 2.4 Предположения и зависимости
1. Разрешение экрана пользователя продукта – 1920x1080.  
2. Для лучшего восприятия отображаемой информации колонки и строки дочерних окон должны иметь чередование оттенков.  
3. Для лучшего восприятия различных типов данных текст разных колонок должен отображаться различными цветами.

<a name="system_requirements"/>

# 3 Системные требования
Информационная автоматизированная система может работать под управлением семейства операционных систем Win32 (Windows 95, Windows 98, Windows 2000, Windows NT и т.д.) с установленной СУБД MySQL.

<a name="functional_requirements"/>

## 3.1 Функциональные требования
1. Создание и просмотр списка товаров.  
2. Поиск товара по различным параметрам в списке товаров.  
3. Добавление товара в список товаров, изменение и удаление товара.  
4. Создание заказа на выбранный товар и просмотр списка заказов.  
5. Поиск заказа по различным параметрам в списке заказов.  
6. Изменение заказа в списке заказов, завершение (удаление) и возврат (отмена) заказа.

<a name="non-functional_requirements"/>

## 3.2 Нефункциональные требования
Приложение должно иметь дружественный дизайн;

<a name="quality_attributes"/>

### 3.2.1 АТРИБУТЫ КАЧЕСТВА
Атрибуты, важные для пользователей:  
1. Доступность-1. Система должна быть доступна как минимум на 99% по рабочим дням, с 8.00 до 22.00 по местному времени, чтобы менеджер интернет-магазина мог осуществлять регистрацию товара и обработку заказов.  
2. Безопасность-1. Все пользователи должны иметь возможность запускать и работать с приложением, так как блокировка неавторизованного доступа осуществляется при запуске операционной системы.  
3. Удобство и простота использования. Всем функциям меню «Файл» должны соответствовать быстрые клавиши, нажимаемые одновременно с Ctrl.  
Атрибуты, важные для разработчиков:  
1. Лёгкость в эксплуатации-1. Вложенность вызываемых функций не должна превышать 10 уровней.  
2. Лёгкость в эксплуатации-2. Для каждого программного модуля непустые комментарии в соотношении к исходному коду должны составлять как минимум 0,1.  
3. Тестируемость-1. Максимальная цикломатическая сложность модуля (количество логических ответвлений в модуле исходного кода) не должна превышать 50.

<a name="security_requirements"/>

### 3.2.2 Требования к безопасности
Надежное функционирование автоматизированной системы должно быть обеспечено выполнением организационно-технических мероприятий, таких как:
- использование лицензионного программного обеспечения;
- организация бесперебойного питания путем использования блоков бесперебойного питания;

Загрузка и отображение основного окна программы не должны превышать 5 секунд.