# Измерение температуры

## Список оборудования 

- ИРТ5200
- Термометр сопротивления 
- Лампочка, 24В

- Произвольное количество реле
- Произвольное число автоматов (переключателей, электрических ключей)

## Теоретическая справка 

Есть несколько способов измерить температуру при помощи электронных устройств. Один из них основан на расширении материала при увеличении температуры, а термометры, основанные на этом методе называются *термометр сопротивления*.

## Вопросы для лучшего понимания происходящего

1. Из какого материала выполнен измеряющий элемент в термометре?
2. Что значит маркировка на термометре?
3. Скорее всего, внутри термометра вы найдете 4 контакта (помимо '+' и '-' для проверки измерений "по току"), но ведь для измерения сопротивления необходимо только 2 контакта?! Зачем нужны оставшиеся 2?

## Задание 

Научитесь снимать значения с термометра сопротивления при помощи ИРТ5200. Сделайте это двумя способами:
	1. По току
	2. Подключив термометр по трехпроводной схеме

Внутри ИРТ есть реле, которые можно настроить (сигнализирующее что-то там). Научитесь зажигать лампочку "К2" на корпусе при достижении температуры в 25 градусов и выше.

Так же, при срабатывании этого реле, внутри замыкается и размыкается некоторый ключ, подключите лампочку к ИРТ так, чтобы при срабатывании реле она загоралась.

Иногда мы хотим иметь "не совсем линейное поведение" устройства в зависимости от показателей (самостоятельно узнайте, что такое гистерезис). Настройте ИРТ на следующее поведение:
	1. При росте температуры лампочка К3 загарается при 25 градусах
	2. Лампочка К3 гаснет в момент, когда температура опускается ниже 22 градусов

При росте температуры от 20 градусов, при 23 градусах лампочка еще не горит, а при падении температуры от 30 градусов, на 22.5 градусах лампочка еще горит

Теперь мы хотим сделать точно такое же поведение, только вместо встроенных функций ИРТ использовать внешние реле.
Используйте ИРТ только в качестве ключей, зависящих от измерений. Для ускорения отладки используйте автоматы, чтобы не греть и остужать термометр каждый раз (увы, это занимает какое-то время).

# Подсказки и идеи

1. Чтобы быстрее остужать термометр, намочите тряпку и помашите ей
2. Вместо лампочки можно взять пневмозаслонки: если температура привысила 25 градусов, воздух обдувает термометр, пока последний не остынет до 22 градусов (получается своего рода холодильник)
3. Схему, в которой реле запитывает само себя, иногда называют "самоподхват реле"
