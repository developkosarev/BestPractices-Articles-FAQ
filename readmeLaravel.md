## LARAVEL

## Contents

### **Использование связки Controller Service Repository Model при работе в Laravel**

Статья [Как вы работаете с Laravel](https://habr.com/ru/post/350778/ "Использование связки Controller Service Repository Model в Laravel") расказывает о том как работать с сервис классом и репозиторием.

### https://klisl.com

Статья [Архитектура Laravel](https://klisl.com/laravel_architecture.html "Архитектура Laravel") 

Статья [Сервис провайдеры](https://klisl.com/laravel_service_providers.html "Сервис провайдеры") 

Статья [Как разделить роли в Laravel](https://habr.com/ru/company/simbirsoft/blog/481796/ "Как разделить роли в Laravel") 

### https://laravel.demiart.ru/tag/laravel/ 

Статья [Паттерн репозиторий](https://laravel.demiart.ru/repository-design-pattern/ "Паттерн репозиторий Laravel") 

Статья [Паттерн сервисный слой в Laravel](https://laravel.demiart.ru/service-layer-design-pattern/) 

Статья [Исключения Laravel: ловим, обрабатываем и создаем собственные](https://laravel.demiart.ru/isklyucheniya-laravel-lovim-obrabatyvaem-i-sozdaem-sobstvennye/)


Статья [Реализация своего интерфейса под способы оплаты](https://ru.stackoverflow.com/questions/943573/%D0%A0%D0%B5%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-%D1%81%D0%B2%D0%BE%D0%B5%D0%B3%D0%BE-%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D1%84%D0%B5%D0%B9%D1%81%D0%B0-%D0%BF%D0%BE%D0%B4-%D1%81%D0%BF%D0%BE%D1%81%D0%BE%D0%B1%D1%8B-%D0%BE%D0%BF%D0%BB%D0%B0%D1%82%D1%8B-laravel)



### Resource в Laravel для API (убрать из модели лишние данные ProductResource) 
Статья [Ресурсы для API в Laravel](https://scotch.io/tutorials/laravel-eloquent-api-resources#toc-prerequisites-)  
Вопросы по ресурсам
https://stackoverflow.com/questions/49494472/laravel-eloquent-resource-collection-response

Статья [Презентары](http://laravel-news.ru/blog/tutorials/presenters-in-laravel)

### **Основые команды Artisan**

1. php artisan key:generate (генерация нового ключа)
2. Добавляем аутентификацию в проект (php artisan make:auth)
3. Создаем модель (php artisan make:model Category -m) 
4. Создаем модель (php artisan make:model Product -m   ключ -m создает миграцию)  

##### **В миграции прописываем вручную все поля и связи**
1. Выполняем миграцию  
(php artisan migrate)  
(php artisan migrate:rollback --step=1  удаляем последнюю миграцию 1шт. )  
(php artisan migrate:rollback    удаляет все)
2. Заполнение тестовыми данными  
(php artisan make:seeder CategoryTableSeeder) 
3. Добавление пустой миграции  
(php artisan make:migration create_foreign_products)
4. Добавление полей в таблицу  
(php artisan make:migration create_parrent_id --table categories)
5. Заполнение таблиц  
(php artisan db:seed          php artisan db:seed --class=UsersTableSeeder)
6. php artisan make:controller ShowProfile --invokable

7. Создаем модель  
(php artisan make:model ExciseStamp -m) 
8. php artisan make:controller api/v1/ExciseStampController --resource --model=ExciseStamp
9. Изменение размера столбцов  
(composer require doctrine/dbal)
10. Выполнить в случае есть класс не найден  
(composer dump-autoload)
11. Laravel debugbar (https://github.com/barryvdh/laravel-debugbar)

##### **API**
1. Создание API контроллера  
(php artisan make:controller api/v1/CategoryController --resource --model=Category)
2. Добавляем путь к api контроллеру в routes\api.php  
(Route::group(['prefix' => '/v1',  'namespace' => 'Api\V1', 'as' => 'api.'], function () {
        Route::resource('companies', 'CompaniesController', ['except' => ['create', 'edit']]);
    });)
3. Создание API контроллера  
(php artisan make:controller api/v1/ProductController --resource --model=Product)	

4. Тестирование https://www.youtube.com/watch?v=5VN-_VjLB5M
5. Создание ролей https://medium.com/@ezp127/laravel-5-4-native-user-authentication-role-authorization-3dbae4049c8a
6. API authentication  https://codebriefly.com/laravel-5-6-custom-token-base-api-authentication/
                       https://softobzor.com.ua/laravel-restful-api/

npm run watch


### **Прочее**

Список команд mysql
https://artkiev.com/blog/mysql-full-list-commands.htm

фаервол
https://bozza.ru/art-259.html

база не видна из вне
https://dev.1c-bitrix.ru/community/forums/forum32/topic96617/

база не видна из вне от пользователя root, нужно создать нового и предоставить привелегии
http://qaru.site/questions/3369/mysql-grant-all-privileges-on-database

mysql -u root -p   (Вход в консоль на linux)

CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password'; 
GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';
FLUSH PRIVILEGES;

//Смена пароля
ALTER USER 'root'@'localhost' IDENTIFIED BY 'new_password'
ALTER USER 'root'@'localhost' PASSWORD EXPIRE NEVER;

Установка composer
https://habr.com/post/197454/


Для виртуральной машине bitrix установить zip
yum install zip
yum install unzip

Отключить все disable в etc/php.d

Перезапуск сети
service httpd restart

Перезапуск ngix 
systemctl restart nginx

Установка minding commander (запуск mc)
yum install mc

меняем путь в appache /etc/http/bx/conf
меняем путь в nginx /etc/nginx/bx/site_enabled
добавляем /public

//Смена разрешения на всех вложенных файлах
chown -R bitrix:bitrix /home/bitrix/www


//Установка Laravel Ubuntu
https://hackernoon.com/a-step-by-step-guide-to-setup-php-laravel-environment-linux-50b55a4fd15e

//Установка web панели 
//http://blog.sedicomm.com/2018/01/22/ustanovka-centos-web-panel-v-centos/

NPM Основные команды
https://habr.com/post/133363/
npm list -g --depth=0 (Глобально установленные пакеты)

//Переход с c# на PHP
https://habr.com/users/GraDea/

//Mobile-Detect Определение устройства с которого открывается сайт
https://github.com/serbanghita/Mobile-Detect

//Установка сервера Ubuntu (web min)
https://www.youtube.com/watch?v=ePw9LQgBAnc
http://webgoal.ru/sistemnoe_administrirovanie/ustanovka_lamp_(linux_apache_mysql_php)_ubuntu_1804_dlya_lokalnoi_razrabotki9.html
sudo apt-get install php-xml
sudo apt-get install php-mbstring

https://www.youtube.com/watch?v=uIXScyhCtPc

//Установка Node js Ubuntu
https://www.digitalocean.com/community/tutorials/node-js-ubuntu-18-04-ru
//авто запуск сайта на node (npm i pm2 -g)
https://habr.com/sandbox/96765/
//Загрузка почты //Работа с почтой, для приема писем по декларации (готовый проект)
https://github.com/ladybirdweb/momo-email-listener
//Ограничение достпа к сайте по IP адресам  (настройка прав)
https://hackware.ru/?p=5413


### **Unit test**

![Настройка unit тестов PHPShtorm](/img/UnitTestPHPStorm.jpg?raw=true)

[Готовые корзины на git](https://github.com/topics/shopping-cart)
