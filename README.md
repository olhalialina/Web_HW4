# Web_HW4
Ваша мета реалізувати найпростіший веб-додаток. За основу взяти наступні файли.

За аналогією з розглянутим прикладом у конспекті, створіть веб-додаток з маршрутизацією для двох html сторінок: index.html та message.html.

Також:

Обробіть під час роботи програми статичні ресурси: style.css, logo.png;

Організуйте роботу з формою на сторінці message.html;
У разі виникнення помилки 404 Not Found повертайте сторінку error.html
Ваша програма працює на порту 3000

Для роботи з формою створіть Socket сервер на порту 5000. Алгоритм роботи такий. Ви вводите дані у форму, вони потрапляють у ваш веб-додаток, який пересилає його далі на обробку за допомогою socket (протокол UDP), Socket серверу. Socket сервер переводить отриманий байт-рядок у словник і зберігає його в json файл data.json в папку storage.

Формат запису файлу data.json наступний:

{
  "2022-10-29 20:20:58.020261": {
    "username": "krabaton",
    "message": "First message"
  },
  "2022-10-29 20:21:11.812177": {
    "username": "Krabat",
    "message": "Second message"
  }
}

Де ключ кожного повідомлення - це час отримання повідомлення: datetime.now(). Тобто кожне нове повідомлення від веб-програми дописується до файлу storage/data.json з часом отримання.

Використовуйте для створення вашої веб-програми один файл main.py. 

Запустіть HTTP сервер і Socket сервер у різних потоках.


Додаткове завдання

​
Це додаткове завдання і його можна не виконувати для здачі цього домашнього завдання.


Створіть Dockerfile та запустіть ваш додаток як Docker-контейнер
За допомогою механізму voluemes, зберігайте дані з storage/data.json не всередині контейнера
