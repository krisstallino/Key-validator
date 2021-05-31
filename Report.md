# Отчёт о тестировании <Credit Card Number Validator>

## Краткое описание

24.05.2021 - 29.05.2021 было проведено функциональное тестирование приложения Credit Card Number Validator.

Приложение проверяет карты согласно алгоритму Луна. Проверяется контрольная цифра - последняя в номере карты. 
Ожидаемо тест будет падать, когда количество цифр в номере карты отличается от 16, т.к. это жестко закреплено в условиях метода, и когда контрольная цифра не пройдет проверку алгоритма.

На тестирование затрачено: 8 часов

В результате тестирования выявлены следующие дефекты:
* [Issue #1](https://github.com/krisstallino/Key-validator/issues/1#issue-907352947)
* [Issue #2](https://github.com/krisstallino/Key-validator/issues/2#issue-907375612)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* [тест кейсы](https://docs.google.com/spreadsheets/d/1lVneSGsB50Slpu5xiSca-b3tEWf0ZOBDQ9I--tkCmxU/edit?usp=sharing)
* [баг репорты](https://github.com/krisstallino/Key-validator/issues)

В качестве тестовых данных использовались данные [FreeFormatter.com](https://www.freeformatter.com/credit-card-number-generator-validator.html):
#### карты МПС Visa:
* 4913622613868495 - Result is OK  
* 4916360047732956 - Result is OK  
* 4716789056801365699 - Result is FAIL

#### карты МПС Visa Electron
* 4175007288091248 - Result is OK  
* 4026109881176474 - Result is OK

#### карты МПС MasterCard
* 5215915988197892 - Result is OK  
* 5494386514925119 - Result is OK  
* 5244151680086216 - Result is FAIL  

#### карты МПС American Express (AMEX)
* 344736977074792 - Result is FAIL  
* 349246228233473 - Result is FAIL

#### карты МПС Maestro
* 6304410309485523 - Result is OK  
* 5020151716180654 - Result is OK

### Тестирование производилось в следующем окружении:
* macOS Big Sur ver.11.3.1
* Java ver.11.0.10
* IntelliJ IDEA CE 2021.1.1