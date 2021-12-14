# Метод или переменная доступны НаКлиенте

Метод или переменная доступны НаКлиенте в модулях менеджера или объекта

## Неправильно

```bsl

Перем ПеременнаяМодуля;

Процедура ПередУдалением(Отказ)
	// Неправильно
КонецПроцедуры

Процедура Неправильно() Экспорт
	// пусто
КонецПроцедуры

ПеременнаяМодуля = Неопределено;

```

## Правильно

```bsl
#Если Сервер Или ТолстыйКлиентОбычноеПриложение Или ВнешнееСоединение Тогда

Перем ПеременнаяМодуля;

Процедура ПередУдалением(Отказ)
	// Неправильно
КонецПроцедуры

Процедура Правильно() Экспорт
	// пусто
КонецПроцедуры

ПеременнаяМодуля = Неопределено;

#Иначе
  ВызватьИсключение НСтр("ru = 'Недопустимый вызов объекта на клиенте.'");
#КонецЕсли
```

## См.

- [Поддержка толстого клиента, управляемое приложение, клиент-сервер](https://its.1c.ru/db/v8std#content:680:hdoc:2)
- [Обработчики событий ОбработкаПолученияПредставления и ОбработкаПолученияПолейПредставления](https://its.1c.ru/db/v8std#content:746:hdoc)