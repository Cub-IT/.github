# Accaunts Use Cases

## Створення облікового запису:
Повинен бути екран реєстрації користувача. Він включає текстові поля:
 - ім'я користувача
 - пошта
 - пароль

У більш пізніх версіях засточунку повинен мати можливість реєстрації за допомогою існуючих облікових 
записів Google, GitHub...

Після введення користувачем даних, повинен надійти запит на сервер.
Запит має містити пошту, яку вказали. Бєк робить перевірку, чи не була вказана пошта зарєстрована до цього.
Якщо пошта не була зарєстрована до цього, то на пошту має прийти лист, де вказано двозначне число,
а також сервер повертає відповідь до клієнта з цим двоцифровим числом.
Якщо пошта була зарєстрована до цього, то бєк повертає відповідь, що реєстрація за даною поштою неможлива.

У разі позитивної відповіді від бєка клієнт показує корситувачу новий екран з полем для вводу двоцифрового числа,
яке користувач може знайти у повідомленні за адресою пошти, яку вказав на попередньому кроці.
Після введення користувачем двоцифрового числа, повинен надійти запит на сервер.
Запит має містити ім'я користувача, пошту та пароль, які були вказані на попередньому кроці.
У разі негативної відповіді від бєка, повина бути виведене повідомлення з описом причини невдачі реєстрації.

Бєк робить перевірку, чи не була вказана пошта зарєстрована до цього.
Якщо пошта не була зарєстрована до цього, то вносить користувача до БД та відправляє відповідь клієнту про
вдале завершення рерєстрації.
Якщо пошта була зарєстрована до цього, то бєк повертає відповідь, що реєстрація за даною поштою неможлива.

У разі позитивної відповіді від бєка на клієнті відбувається вхід до облікового запису, користувач переходить на екран списку груп, 
у яких він є учасником. (Якщо таких груп немає, то це має бути явно вказано.) У разі негативної відповіді, 
показати користувачеві причину невдачі та очікувати на нову спробу.

## Вхід до облікового запису:
Має бути екран входу користувача. Він включає текстові поля:
 - пошта
 - пароль

У більш пізніх версіях засточунку повинен мати можливість входу за допомогою існуючих облікових записів Google, GitHub...

Після введення користувачем даних, повинен надійти запит на сервер. 
Запит має містити пошту та пароль, введені користувчем.
Бєк робить перевірку на співпадіння пошти та паролю зі записом у БД.
У разі співпадіння, бєк відправляє позитивну відповідь, інакше - причину невдачі.
У разі позитивної відповіді від бека відбувається вхід до облікового запису, користувач переходить на екран списку груп, в яких він є учасником.
(Якщо таких груп немає, то це має бути явно вказано.) У разі негативної відповіді, показати користувачеві причину невдачі 
та очікувати на нову спробу.
