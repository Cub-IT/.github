# Group Use Cases

## Створення групи
Повинен бути екран додавання групи (він може бути у формі свпливаючого вікна/діалогу).
Він включає текстові поля:
 - назва групи (обов'язково не може бути пустим при ство).

Поле назви групи не може бути порожнім при заповненні (або складатися тільки з пробілів).

Після надсилання форми, клієнт має надіслати запит на сервер.
Запит має містити назву групи та користувача, який додає цю групу.

Бек створює нову групу на основі цих даних та додає запис до БД.
Оскільки БД реалізує паттерн Observer, то повідомлення про зміну інформації в БД має прийти
на клієнт автоматично. Клієнт має відобразити ці зміни.

## Запрошення учасників до груп
Приєднання користувачів до класу здійснюється за допомогою коду, який генерується на основі
назви групи, пошти учасника, який створив цю групу та дати створення групи.

У тільки у власника групи є можливість дізнатися код класу.
Власник може надати код класу іншим користувачам, які можуть під'єднатися до цього класу
за допомогою цього коду класу.

Для приєднання користувача до класу, має існувати окремий екран приєднання до класу
(він може бути у формі свпливаючого вікна/діалогу).
Коли користувач вводить код класу, клієнт має надіслати запит на сервер.
Запит включає у себе код групи.
Сервер, у свою чергу, перевіряє, чи існує група з таким кодом групи та додає нового
учасника до цієї групи. Після цього сервер надсилає у відповідь клієнту id групи.
У разі, якщо групи з таким кодом групи не існує, то сервер надсилає відповідь клієнту
про невдачу.

Клієнт, у разі отримання кода групи від сервера, показує повідомлення, що приєднання до групи
вдалося.
У разі отримання повідомлення про невдачу, клієнт показує повідомлення з причиною невдачі.
