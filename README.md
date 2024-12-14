### Проект представляет собой веб приложение для поиска рецептов по ингредиентам.

### Основные технологии

- Laravel 8 для backend разработки
- MySQL для базы данных
- Blade шаблонизатор для управления представлениями

### Инструкции по установке

1. Склонировать репозиторий на локальную машину в папку domains в OpenServer с помощью git clone
![image](https://github.com/user-attachments/assets/f9fd06aa-44e1-4105-8c42-3ece5bd74d08)
2. В настройках Open server в пункте "Домены" Выбрать "Ручное управление" и добавить путь к папке public. Результат показан на скриншоте
![image](https://github.com/user-attachments/assets/72f13e2c-d9bf-469a-85c2-8a14c257ec1d)
3. Зайти в PhpMyAdmin и создать БД с произвольным именем
4. Настройте файл `.env` для подключения к базе данных, как показано на скриншоте.
![image](https://github.com/user-attachments/assets/b6fa88aa-e5d5-4c2c-9f50-344accbca7b6)
5. Откройте консоль OpenServer, перейдите в папку проекта, и выполните следующие команды:
6. Установите зависимости командой `composer install`.
7. Сгенерируйте ключ с помощью `php artisan key:generate`.
8. Выполните миграции командой `php artisan migrate`.
9. Запустите веб-сервер с помощью `php artisan serve`'

### Инструкции по внесению изменений в проект

1. Выполнить комманду `git pull` чтобы получить актуальную версию проекта на локальной машине
2. Устранить проблемы, если они есть (Удобно делать в Visual studio code, например. Рекомендую поставить расширение GitLens).
3. `git add -A` - добавить все изменения
4. `git commit -m '*комментарий'` - сделать коммит изменений
5. `git push` - загрузить изменения
6. Выщеперечисленные команды удобнее сделать в интерфейсе через GitLense

По умолчанию сервер доступен по адресу: http://127.0.0.1:8000/
