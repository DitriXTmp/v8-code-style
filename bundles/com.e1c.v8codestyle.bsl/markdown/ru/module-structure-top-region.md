# Стандартная область структуры модуля верхнеуровневая

Проверяет что стандартная область структуры модуля не является вложенной

## Неправильно

```bsl

#Область НеПустая

#Область ПрограммныйИнтерфейс

Процедура Тест() Экспорт
	
КонецПроцедуры

#КонецОбласти

#КонецОбласти

```

## Правильно

```bsl

#Область ПрограммныйИнтерфейс

Процедура Тест() Экспорт
	
КонецПроцедуры

#КонецОбласти

```

## См.


- [Структура модуля](https://its.1c.ru/db/v8std#content:455:hdoc)
