## План тестирования возможности записи на обучение профессии "Тестировщик ПО".

### Объект тестирования: обучение профессии "Тестировщик ПО" на веб-сайте [Нетология](https://netology.ru/) c формой записи на курс [Тестировщик ПО](https://netology.ru/programs/qa).

#### Предусловия:

Переход к форме записи на курс "Тестировщик ПО":

- Открыть стартовую страницу сайта Нетология (https://netology.ru/)

- Есть несколько способов перехода к форме записи на курс:

1. В левом верхнем углу нажать на PopUp `"Каталог курсов"`, навести курсор на категорию `"Программирование"`, нажать на категорию `"Тестировщик ПО"`, нажать на кнопку `"Записаться"`, происходит автоматический проскролл к форме записи на курс.

2. На главной странице веб-сайта Нетология нажать на категорию `"Программирование"`,нажать на профессию `"Тестировщик ПО"`, нажать на кнопку `"Записаться"`, происходит автоматический проскролл к форме записи на курс.

3. На главной странице веб-сайта Нетология нажать на категорию `"Программирование"`, в поле поиска `"Чему вы хотите научиться?"` каталога курсов ввести "Тестировщик ПО", нажать на курс `"Тестировщик ПО"`, нажать на кнопку `"Записаться"`, происходит автоматический проскролл к форме записи на курс.

4. В левом верхнем углу нажать на PopUp `"Каталог курсов"`, нажать на кнопку `"Полный каталог"` , нажать на категорию `"Тестировщик ПО"`, нажать на кнопку `"Записаться"`, происходит автоматический проскролл к форме записи на курс.

5. В левом верхнем углу нажать на PopUp `"Каталог курсов"`, нажать на кнопку `"Полный каталог"` , в поле поиска `"Чему вы хотите научиться?"` каталога курсов ввести "Тестировщик ПО", нажать на курс `"Тестировщик ПО"`, нажать на кнопку `"Записаться"`, происходит автоматический проскролл к форме записи на курс.

#### Тестовые сценарии:

##### Позитивные:

###### пользователь не зарегистрирован или не авторизован на сайте

- В поле «Имя» ввести валидное значение имени (короткое имя, длинное имя, имя в нижнем регистре, имя в верхнем регистре двойное имя через дефис, двойное имя через пробел, имя с буквой Ё, зарубежное имя, имя на латинице)
- В поле с номером телефона ввести валидное значение для номера телефона (Номер в формате +9 (999) 999-99-99)
- В поле «Электронная почта» ввести валидное значение электронной почты (Email в нижнем регистре, Email в верхнем регистре, Email с цифрами в имени аккаунта или в доменной части, Email с дефисом в имени аккаунта или доменной части, Email с точками в имени аккаунта, Email с несколькими точками в доменной части

**Ожидаемый результат:** На электронный адрес приходит письмо с подтверждением заявки. Переход на страницу оплаты.

###### пользователь зарегистрирован и авторизован на сайте

- В поле «Имя» ввести действительное значение имени (короткое имя, длинное имя, имя в главном регистре, имя в записи регистра, двойное имя через дефис, двойное имя через пробел, имя с буквой Ё, зарубежное имя, имя на латинице)
- В поле с номером телефона введите действительное значение для номера телефона (Номер в формате +9 (999) 999-99-99)

**Ожидаемый результат:** На зарегистрированный адрес электронной почты приходит письмо с подтверждением заявки. Переход на страницу оплаты.

##### Негативные:

1. Оставить поле/поля формы/форм пустыми. **Ожидаемый результат:**  форма не отправляется, поле/поля подсвечиваются с ошибкой "Обязательное поле".
2. Заполнить поле "Имя" не валидными данными (одна буква, спе.символы в имени, длинна более 128 символов, иероглифы вместо кириллици или латиницы, пробелы вместо букв). **Ожидаемый результат:** имя некорректное, поле «Имя» подсвечивается красным цветом, сообщение об ошибке: «Должно состоять из букв»
3. Заполнить поле "Номер телефона" не валидными данными (номер телефона без знака + в начале, номер телефона более/менее 11 цифр). **Ожидаемый результат:** поле «Номер телефона» подсвечивается красным цветом, сообщение об ошибке: «Номер в формате +9 (999) 999-99-99».
4. Заполнить поле "Электронная  почта" не валидными данными (Превышение длинны Email(более 320 символов), адрес почты без знака @ , пробелы в имени и/или доменной части, отсутствие точки в доменной части, Email без имени или доменной части, некорректный домен первого уровня (допустимо 2-63 букв после точки)). **Ожидемый результат:** поле «Электронный адрес» подсвечивается красным цветом, сообщение об ошибке: «Неверный email».

* (Для авторизованого пользователя отсутствует поле "Электронная почта", поэтому тесты для проверки этого поля отсутствуют)
### Перечень используемых инструментов:

1. `IntelliJ IDEA`- интегрированная среда разработки ПО для многих языков программирования. Удобная среда подготовки авто-тестов.
2. `Java 11` - объектно-ориентированный язык программирования, оптимальный для написания понятных и наглядных автотестов.
3. `JUnit 5` - инструмент тестирования, среда модульного тестирования для языка программирования Java.
4. `Gradle` - мощная и простая система автоматической сборки проектов, которая используется для упрощения работы с JAVA.
5. `Selenide` - это фреймворк для автоматизированного тестирования веб-приложений на основе Selenium WebDriver, дающий следующие преимущества: изящный API, поддержка AJAX для стабильных тестов, мощные селекторы, простая конфигурация.
6. `Faker` - это библиотека, которая позволяет генерировать случайные данные. С ее помощью можно заполнить таблицы в базе данных, построить корректные XML-документы, сформировать JSON-ответы для REST.

### Перечень необходимых разрешений/данных/доступов:

1. Разрешение на проведение тестирования и автоматизации на веб-сайте [Нетология](https://netology.ru/)
2. Необходим доступ к API и БД (доступ к действующей базе данных несет определенные риски) для проверки результатов выполнения тестов.
3. Техническая документация, для понимания валидных и невалидных данных.

### Перечень и описание возможных рисков при автоматизации:

1. Отсутствие технической документации.
2. Незначительное изменение реализации веб-элементов на странице, могут привести к падению ранее написаных авто-тестов.
3. Авто-тесты не проверяют графический интерфейс (GUI) сайта.
4. Возможен "Мусор" в базе данных.
5. Ложные срабытывания по отправке форм, что в свою очередь может увеличить нагрузку по обработке данных

### Перечень необходимых специалистов для автоматизации:

Один junior-специалист.

### Интервальная оценка с учетом рисков (в часах):

Справится за час в течении недели.