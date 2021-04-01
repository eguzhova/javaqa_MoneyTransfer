### Отчёт о тестировании Money Transfer

#### Краткое описание
 1 апреля 2021 было проведено функциональное тестирование приложения Money Transfer.

На тестирование затрачено: 2 часа

В результате тестирования выявлены следующие дефекты:
* [Ошибка вычисления итогового баланса после перевода](https://github.com/eguzhova/javaqa_MoneyTransfer/issues/1)

#### Описание процесса тестирования
В процессе тестирования использовался тестовый сценарий:

1. Создать проект в IntelliJ IDEA с кодом
```java
public class Main {

    public static void main(String[] args) {
        int currentBalance = 2_000_000_000;
        int transferAmount =  500_000_000;
        int balanceAfterTransfer = currentBalance + transferAmount;
        System.out.println("Баланс после перевода:"+balanceAfterTransfer);
    }
}
```
2. Запустить код на исполнение
2. Оценить правильность результата

**Тестовые данные:**
1. Исходный баланс: 2 000 000 000
1. Сумма перевода на счет: 500 000 000

#### Тестирование производилось в следующем окружении:
* MacOS 11.2.3 (20D91)
* openjdk version "11.0.10" 2021-01-19
* IntelliJ IDEA Community Edition "2020.3.3"
