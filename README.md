
Проект Foodgram позволяет пользователям публиковать рецепты, добавлять рецепты в избранное и список покупок, подписыватся на других пользователей и скачивать список продуктов.

Проект доступен по адресу: 

http://178.154.223.18/

Доступ в админку для суперюзера:

login - admin@ya.ru
pass - 1212

Доступ в ЛК для обычного пользователя:

login - test@ya.ru
pass - Test1212

Запуск проекта на сервере
Для работы сервиса на сервере должны быть установлены Docker и docker-compose

    Клонируйте репозиторий командой:

git clone https://github.com/r9fq56/foodgram-project-react.git

    Перейдите в каталог командой:

cd foodgram-project-react/backend/

    Выполните команду для запуска контейнера:

docker-compose up -d

    Выполните миграции:

docker-compose exec web python manage.py makemigrations --noinput
docker-compose exec web python manage.py migrate --noinput

    Команда для сбора статики:

docker-compose exec web python manage.py collectstatic --no-input

    Команда для создания суперпользователя:

docker-compose exec web python manage.py createsuperuser

