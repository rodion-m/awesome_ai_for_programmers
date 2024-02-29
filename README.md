# Awesome AI for Programmers
В этом репозитории я собираю все самое интересное на тему применения AI в разработке ПО.

## Кейсы применения ChatGPT для разработчиков
1. Написание кода по задачи, добавление фичи к имеющемуся коду - например, написание функции, которая сортирует список по возрастанию.
    1. Рефакторинг (разбиение длинного метода на несколько коротких) - например, разбиение длинного метода, который получает список пользователей и возвращает число пользователей с активными аккаунтами, на несколько коротких методов.
    Универсальный промпт: `Rewrite code like you are a Senior Software Engineer. Fix all code smells. Make this code perfect.`
    2. Оптимизация
2. Написание тестов для кода, генерация тестов для интерфейса - например, написание тестовых сценариев для функции, которая возвращает сумму элементов в списке.
  1. Промпт для именования тестов в соответствии с правилами, изложенными в книге "Принципы юнит тестирования" Владимира Хорикова ниже.
3. [Написание кода к тестам](https://github.com/di-sukharev/AI-TDD) (TDD) - например, написание тестовых сценариев для функции, которая проверяет, является ли число простым.
4. Написание и оптимизация SQL запросов - например, написание SQL запроса, который находит количество пользователей, зарегистрированных в определенный день.
5. Конвертация SQL кода в запросы Entity Framework и наоборот - например, конвертация SQL запроса в запрос Entity Framework, который получает список пользователей, у которых есть задолженности по оплате.
6. Анализ кода: поиск стилистических ошибок, ошибок асинхронности/многопоточности - например, поиск неэффективных запросов в коде, который забирает данные из базы данных.
7. Объяснение кода - например, объяснение работы алгоритма поиска кратчайшего пути в графе.
8. Развернутая информация об ошибках - например, вывод развернутой информации об ошибке, которая произошла во время выполнения приложения.
9. Рисование диаграмм и графов (mermaid, [quickchart.io](http://quickchart.io/), Graphviz) - например, создание диаграммы классов для приложения.
10. Генерация данных - например, генерация массива из слов из медицинской тематики, который используется в качестве исходных данных для приложения.
11. Добавление документации к методам - например, добавление документации к методу, который возвращает среднее значение элементов в списке.
12. Генерация документации из кода в markdown (dto to markdown) - например, генерация документации из комментариев к коду в формате markdown.
13. Конвертация кода из разных языков - например, конвертация кода на Python в код на C++.
14. Конвертация json в xml и обратно - например, конвертация json файла, который содержит информацию о пользователе, в xml файл и обратно.
15. Генерация классов из json - например, генерация классов, которые представляют сущности в приложении, на основе json файла, который содержит информацию об этих сущностях.
16. Оценка вычислительной сложности кода
17. Экранирование данных для кода: например, иногда нужно json закинуть в строковую переменную или из другого кода сделать строку
18. Генерация реализации класса по контракту интерфейса

### Промпт для именования тестов
<details>
  <summary>Показать промпт для именования тестов по правилам, описанным в книге В. Хорикова "Принципы юнит-тестирования"</summary>
You are a test namer. The user send you the tests names and you rename it ACCORDING to these rules:

- **No rigid naming policy**: Avoid using a strict naming convention, as it may not provide a high-level description of complex behavior. Allow freedom of expression.
- **Describe the scenario in plain English**: Name the test as if you were describing the scenario to a non-programmer who is familiar with the problem domain, such as a domain expert or a business analyst.
- **Separate words by underscores**: Use underscores to improve readability, especially for long test names.
- **Don't include the method under test in the test name**: Focus on testing application behavior rather than specific code or methods.

Here are some examples to illustrate the transformation from a rigid naming convention to a more expressive and readable test name:

**Rigid naming convention example:**
`public void Sum_TwoNumbers_ReturnsSum()`

**Expressive and readable test name example:**
`public void Sum_of_two_numbers()`

**Another example:**

**Rigid naming convention example:**
`SaveMessages_Throws_Exception_When_UserId_Is_Null`

**Improved test name example:**
`Save_messages_with_null_user_id_is_invalid`

**Another example:**

**Rigid naming convention example:**
`public void IsDeliveryValid_InvalidDate_ReturnsFalse()`

**Improved test name example (step by step):**
1. `public void Delivery_with_invalid_date_should_be_considered_invalid()`
2. `public void Delivery_with_past_date_should_be_considered_invalid()`
3. `public void Delivery_with_past_date_should_be_invalid()`
4. `public void Delivery_with_past_date_is_invalid()`
5. `public void Delivery_with_a_past_date_is_invalid()`


</details>
