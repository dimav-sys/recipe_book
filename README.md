### Проект RecipeBook представляет собой веб приложение для поиска рецептов по ингредиентам.



### Основные технологии

- Laravel 8 для backend разработки
- MySQL для базы данных
- Blade шаблонизатор для управления представлениями



### Инструкции по установке

1. Склонировать репозиторий на локальную машину в папку domains в OpenServer с помощью git clone
![image](https://github.com/user-attachments/assets/f9fd06aa-44e1-4105-8c42-3ece5bd74d08)
2. В настройках Open server в пункте "Домены" Выбрать "Ручное управление" и добавить путь к папке public. Результат показан на скриншоте
![image](https://github.com/user-attachments/assets/72f13e2c-d9bf-469a-85c2-8a14c257ec1d)
3. Запустите Open Server от имени администратора. Зайдите в настройки, выберите раздел модули. Укажите версию MySQL и сохранитесь
4. Сделайте так, чтобы версии http, php и MySQL совпадали
![image](https://github.com/user-attachments/assets/9bccc563-ab3b-4794-bc61-2b04da7dc150)
5. Зайти в PhpMyAdmin и создать БД с произвольным именем
6. Переименуйте файл .env.example в .env
7. Настройте файл `.env` для подключения к базе данных, как показано на скриншоте.
![image](https://github.com/user-attachments/assets/b6fa88aa-e5d5-4c2c-9f50-344accbca7b6)
8. Откройте консоль OpenServer, перейдите в папку проекта, и выполните следующие команды:
9. Установите зависимости командой `composer install`.
10. Сгенерируйте ключ с помощью `php artisan key:generate`.
11. Выполните миграции командой `php artisan migrate`.



### Описание структуры проекта (када жмать штобы что то сделать)

1. `routes/web.php` - маршруты. При переходе пользователя по ссылке с данным маршрутом, ответ генерируется соответствующим методом соответствующего контроллера
2. `app/Http/Controllers` - контроллеры. В своих методах обрабатывают информацию и возвращают пользователю ответ
3. `resources/views` - странички, которые отдаются пользователю. В них зачастую подставляются данные с помощью PHP. Также, в `resources` лежат css, js и всё такое
4. `app/Http/Models`, `database/migrations` - миграции

В принципе, это всё что нужно знать для того чтобы создать что-то не слишком сложное.



### Инструкции по внесению изменений в git репозиторий

1. !!! Выполнить комманду `git pull` чтобы получить актуальную версию проекта на локальной машине
2. Устранить проблемы, если они появились после `git pull` (Удобно делать в Visual studio code, например. Рекомендую поставить расширение GitLens). Проблемы могут появиться, например, если вы уже поменяли файл, и в новой версии файла, который вы скачали он также был изменён. Возникнет конфликт, так как не понятно, какой файл сейчас актуален. Если у вас лапки, можете убрать ваши изменения, выполнить `git pull`, и затем обратно внести изменения, но это неудобно. Лучше Visual studio code с GitLens.
3. `git add -A` - добавить все изменения
4. `git commit -m '*комментарий'` - сделать коммит изменений
5. `git push` - загрузить изменения
6. Выщеперечисленные команды удобнее сделать в интерфейсе через GitLense



### Полезные команды

- `php artisan migrate` - миграция в БД. (на основе моделек в программе строится база данных)
- `php artisan migrate:rollback` - откат миграции
- `php artisan migrate:refresh`      -   перезалить миграции
- `php artisan make:model -m Categoty`   -   создаёт сразу и модель и миграцию (рекомендуется в большенстве случаев)
- `php artisan make:migration create_products_table` - создаёт миграцию отдельно
- `php artisan make:model Product` - создаёт модель отдельно
- `php artisan make:controller CategoryController` - создаёт новый контроллер



### Дополнительная информация

!!! Для создания моделей, миграций и контроллеров используем команды attisan (представлены выше), ручками тоже можно, но так легко ошибиться.

Для запуска проекта откройте пункт "Мои проекты" в Open server и выберите проект. (Или запустите веб-сервер с помощью `php artisan serve`). 

По умолчанию сервер доступен по адресу: http://127.0.0.1:8000/
