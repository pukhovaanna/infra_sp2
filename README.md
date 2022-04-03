# Описание сервиса
Проект **YaMDb** собирает отзывы пользователей на произведения. 
Произведения делятся на категории: «Книги», «Фильмы», «Музыка».

# Шаблон наполнения .env файла
DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
DB_NAME=postgres # имя базы данных
POSTGRES_USER=postgres # логин для подключения к базе данных
POSTGRES_PASSWORD=postgres # пароль для подключения к БД
DB_HOST=db # название сервиса (контейнера)
DB_PORT=5432 # порт для подключения к БД 

# Алгоритм установки сервиса
1. Скопируйте проект на свой компьютер ``` git clone https://github.com/pukhovaanna/infra_sp2.git ```
2. Создайте и активируйте виртуальное окружение: 
```python -m venv venv```, ```source venv/Scripts/activate```
3. Установите зависимости: ```pip install -r requirements.txt```
4. Перейдите в директорию infra/ и:
- запустите контейнеры ```docker-compose up -d --build```
- выполните миграции ```docker-compose exec web python manage.py migrate```
- создайте суперпользователя ```docker-compose exec web python manage.py createsuperuser```
- соберите статику ```docker-compose exec web python manage.py collectstatic --no-input```
# Описание команды для заполнения базы данными
Описание команд можно увидеть в файле _redoc.html_ или по ссылке http://localhost/redoc

# Авторы проекта:
- Анна Пухова
- Юрий Брагин
- Дмитрий Брындин
