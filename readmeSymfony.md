## Symfony

## Contents

### **Работа с базой данных как в 1С**
Статья [Работа с документами как в 1С](https://www.thinktocode.com/2018/03/05/repository-pattern-symfony/)  

### **Мультиязычность**

Статья [Мультиязычность в Symfony](https://phrase.com/blog/posts/symfony-4-i18n/ "Использование связки Controller Service Repository Model в Laravel") Мультиязычность в Symfony.  
Статья [Мультиязычные маршруты](https://symfony.com/blog/new-in-symfony-4-1-internationalized-routing) "Настройка маршрутов"  
Статья [Мультиязычное API] (https://medium.com/q-software/multilingual-symfony-api-b31fa5f204fe) "Мультиязычное API"  

https://stackoverflow.com/questions/27216067/how-to-implement-a-nice-solution-for-multilang-entity-slug-based-routes-in-symfo  
https://github.com/Atlantic18/DoctrineExtensions  

https://stackoverflow.com/questions/52740255/redirect-route-to-language-prefix-in-symfony-4
https://symfony.com/doc/2.6/cookbook/routing/redirect_in_config.html

Статья [API VUE JS] (https://thecodingmachine.io/building-a-single-page-application-with-symfony-4-and-vuejs) "Vue symfony 4 todo"  
Статья [Autentification with VueJs] https://stefanoalletti.wordpress.com/2019/08/05/authentication-with-vuejs-using-symfony-and-api-platform-part-2/  


### **Server start**

01 php -S localhost:8000 -t public  
02 yarn encore dev-server --hot --host symfony002.local  

02 php bin/console server:start  
03 php bin/console server:start 192.168.0.1:8080  

04 if you want to appach, you need add this *composer require symfony/apache-pack*  

### **Doctrine, migration** 

01 php bin/console make:migration  
02 php bin/console doctrine:migrations:migrate  
03 php bin/console doctrine:schema:validate  
04  php bin/console doctrine:schema:update --force  

Статья [Расширения сущностей](http://jstructure.com/post/doctrine-entity-extending/)  
 
### **Controllers** 
 
01 php bin/console make:controller BrandNewController 

### **Router** 

01 php bin/console debug:router
 
### **Fixtures** 

01 Make fixtures php bin/console make:fixtures  
02 Load fixtures php bin/console doctrine:fixtures:load  
03 Help fixtures php bin/console doctrine:fixtures:load --help  
04 Group    php bin/console doctrine:fixtures:load --group=group1 --group=group2  
public static function getGroups(): array
{
	return ['group1', 'group2'];
}  
https://symfony.com/blog/new-in-fixturesbundle-group-your-fixtures

### **Cache** 

01 php bin/console cache:clear

### **Command** 

01 php bin/console app:create-user

### **Pagination** 

https://www.binpress.com/custom-pagination-php-symfony/