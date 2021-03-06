# План автоматизации тестирования сценария перехода к форме записи и заполнения этой формы
### 1) Перечень автоматизируемых сценариев
**Навигация (поиск необходимого курса):**
1) **Сценарий 1:**
  * Зайти на сайт https://netology.ru/ 
  * Выбрать "Каталог курсов"
  * Выбрать "Программирование"
  * Выбрать курс "Тестировщик ПО"
  * на новой странице найти форму для записи
2) **Сценарий 2:**
  * Зайти на сайт https://netology.ru/ 
  * Кликнуть на "Изучайте актуальные темы" 
  * Выбрать "Программирование"
  * Выбрать курс "Тестировщик ПО"
  * на новой странице найти форму для записи 
3) **Сценарий 3:**
  * зайти на сайт https://netology.ru/ 
  * Кликнуть на значок "НЕО"
  * В фильтре выбрать "Программирование", "Профессии" 
  * Выбрать курс "Тестировщик ПО"
  * на новой странице найти форму для записи  

  **Тестирование формы "Записаться на курс":**  
  * **Сценарий 1: ввод всех валидных данных:**
    * имя: имя на кириллице
    * телефон: 11 цифр, начиная с +7/8
    * почта: имя почтового ящика на латинице, @, доменное имя почтового сервера (напрмер, support@netology.ru)
    * нажать кнопку «Записаться».
    * <ins> Ожидаемый результат:</ins> всплывает окошко с подтверждением записи, на телефон/ почту пользователя приходит уведомление об успешной записи на курс
  * **Сценарий 2: отправка формы с пустыми полями:**
    * поля имя, телефон, почта оставить пустыми
    * нажать кнопку «Записаться».
    * <ins> Ожидаемый результат:</ins> всплывает уведомление "Обязательное поле", запись невозможна без заполнения обязательных полей
  * **Сценарий 3: отправка формы с невалидным номером телефона:**
    * имя: имя на кириллице
    * телефон: латинские буквы/символы
    * почта: имя почтового ящика на латинице, @, доменное имя почтового сервера (напрмер, support@netology.ru)
    * нажать кнопку «Записаться».
    * <ins> Ожидаемый результат:</ins> всплывает уведомление "Номер в формате +9 (999) 999-99-99"
  * **Сценарий 4: отправка формы с именем на иностранном языке:**
    * имя: имя на латинице
    * телефон: 11 цифр, начиная с +7/8
    * почта: имя почтового ящика на латинице, @, доменное имя почтового сервера (напрмер, support@netology.ru)
    * нажать кнопку «Записаться».
    * <ins> Ожидаемый результат:</ins> всплывает уведомление "Введите имя на кириллице"
  * **Сценарий 5: отправка формы с некорректным адресом почты:**
    * имя: имя на кириллице
    * телефон: 11 цифр, начиная с +7/8
    * почта: символы/цифры
    * нажать кнопку «Записаться».
    * <ins> Ожидаемый результат:</ins> всплывает уведомление "Неверный email адрес"
### 2) Перечень используемых инструментов с обоснованием выбора
  * Java11 - язык написание кода и автотестов
  * JUnit5 — библиотека для модульного тестирования на языке Java
  * Git, GitHub - хранилище кода
  * Faker - библиотека для генерации тестовых данных
  * Selenide - инструмент автоматизации действий браузера
  * Docker - ПО для развёртывания и управления контейнерами приложения
  * Maven/Appveyor - инструменты для сборки и тестирования ПО
  * Gradle/Allure/Report Portal - инструменты для репортинга и генерации отчетов

### 3) Перечень необходимых разрешений/данных/доступов
* разрешение на автотестирование сайта, на доступ к БД
* доступ к необходимой документации (ТЗ, требования, окружение)
* доступ к БД (для получения, обновления, проверки данных пользователей)
* доступ к тестовому режиму (если система сложная и время позволяет: посмотреть на ее поведение с тестовыми данными, протестировать в "безопасных" условиях)

### 4) Перечень и описание возможных рисков при автоматизации

  * низкая скорость Интернета
  * отсутствие понятного ТЗ, необходимой технической документации
  * отличие реальных данных пользователей от тестовых (тестирование тестовых данных, а не реальных)
  * отсутствие css селекторов на странице для написания тестов
  * отсутствие доступа к БД
  * падение сервера

### 5) Перечень необходимых специалистов для автоматизации
* QA engineers - опытные специалисты по автоматизированному тестированию, знающие программирование, умеющие писать код и внедрять его в новый проект
* ручные инженеры - специалисты разного уровня квалификации, владеющие азами тестирования и разработки ПО, готовые учиться и оптимизировать свою работу 
* программисты/ разработчики - специалисты, отлично разбирающиеся в коде, которые помогут тестировщикам разобраться в программирвании

### 6) Интервальная оценка с учётом рисков (в часах)
60

