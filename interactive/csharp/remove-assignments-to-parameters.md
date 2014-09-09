remove-assignments-to-parameters:csharp

###

1. Создайте локальную переменную и присвойте ей начальное значение вашего параметра.

2. Замените использование параметра в теле метода вашей локальной переменной.



###

```
int Discount(int inputVal, int quantity, int yearToDate)
{
  if (inputVal > 50)
  {
    inputVal -= 2;
  }
  if (quantity > 100)
  {
    inputVal -= 1;
  }
  if (yearToDate > 10000)
  {
    inputVal -= 4;
  }

  return inputVal;
}
```

###

```
int Discount(int inputVal, int quantity, int yearToDate)
{
  int result = inputVal;

  if (inputVal > 50)
  {
    result -= 2;
  }
  if (quantity > 100)
  {
    result -= 1;
  }
  if (yearToDate > 10000)
  {
    result -= 4;
  }

  return result;
}
```

###

Set step 1

# Давайте рассмотрим <i>Удаление присваиваний параметрам</i> на примере небольшого метода расчёта скидки.

Select "inputVal" in parameters of "Discount"

#+ Обратите внимание на параметр <code>inputVal</code>.

Select 3nd "inputVal"
+Select 4th "inputVal"
+Select 5th "inputVal"

#^= Значение этого параметра изменяется в теле метода.

Set step 2

#^ Заменим использование параметра новой переменной, значение которой мы будем изменять, после чего вернем её как результат этого метода.

Go to the start of "Discount"

Print:
```

  int result = inputVal;

```

Select "int result = inputVal"

# Инициализируем нашу переменную значением параметра.

Select 4th "inputVal"
+Select 5th "inputVal"
+Select 6th "inputVal"
+Select 7th "inputVal"

# В теле метода заменим все обращения к параметру на созданную нами переменную.

Print "result"

#C Запускаем финальную компиляцию.

#S Отлично, все работает!

Set final step

#Q На этом рефакторинг можно считать оконченным. В завершение, можете посмотреть разницу между старым и новым кодом.