# api_final
Проект API сервис написан для взаимодействия с проектом Yatube.

С помощью данного проекта можно 
 - добавлять/обновлять/удалять/просматривать посты
 - добавлять/обновлять/удалять/просматривать комментарии к постам
 - получать информацию и списки существующих сообществ
 - производить/просматривать подписки на авторов

Клонируйте репозиторий на своё устройство:
- git clone https://github.com/yandex-praktikum/kittygram2plus.git

Перейдите в директорию:
- cd api_final_yatube

Разверните виртуальное окружение:
- python -m venv env или source env/bin/activate 

Обновите pip:
- python -m pip install --upgrade pip

Установите зависимости из файла requirements.txt:
- pip install -r requirements.txt

Выполнить миграции:
- python3 manage.py migrate

Запустить проект:
- python manage.py runserver

Примеры запросов:

Запросы к постам проекта:



GET: http://127.0.0.1:8000/api/v1/posts/ - весь список постов
POST запрос по данному эндпоинту создаст новый пост
{
  "text": "string",
  "image": "string",
  "group": 0
}

POST: http://127.0.0.1:8000/api/v1/jwt/create/ - создать токен для пользователя

{
"username": "string",
"password": "string"
}

POST: http://127.0.0.1:8000/api/v1/jwt/create/ - активация токен для пользователя

{
"token": "string"
}

POST: http://127.0.0.1:8000/api/v1/jwt/refresh/ - обновить токен для пользователя

{
"refresh": "string"
}