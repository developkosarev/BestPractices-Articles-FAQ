## PHP

## Contents

Статья [Прием платежей на сайте](https://webformyself.com/minikurs/php/index-subscribe.html)

Регулярные Выражения [Регулярные Выражения](https://medium.com/nuances-of-programming/%D1%88%D0%BF%D0%B0%D1%80%D0%B3%D0%B0%D0%BB%D0%BA%D0%B0-%D0%BF%D0%BE-%D1%80%D0%B5%D0%B3%D1%83%D0%BB%D1%8F%D1%80%D0%BD%D1%8B%D0%BC-%D0%B2%D1%8B%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%D0%BC-%D0%B2-%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%D0%B0%D1%85-53820a5f3435)


## XDEBUG
https://gist.github.com/odan/1abe76d373a9cbb15bed
https://www.youtube.com/watch?v=yiQbJG_dSIc
https://www.youtube.com/watch?v=_ua_O01IICg

Работающая отладка

php.ini
[xdebug]
zend_extension = D:\xampp\php\ext\php_xdebug-2.6.1-7.2-vc15.dll
xdebug.remote_enable=1
xdebug.remote_port=9001
xdebug.idekey=PHPSTORM

xampp-win32-7.2.7-0-VC15-installer.exe

http://symfony003.local/?XDEBUG_SESSION_START=17432


### PHPUnit

Обновление php unit в xampp
https://stackoverrun.com/ru/q/11876059

запуск теста из командной строки
d:\xampp\htdocs\symfony003parser>phpunit tests\AppBundle\Controller\DefaultControllerTest.php
d:\xampp\htdocs\symfony003parser>phpunit tests
d:\xampp\htdocs\symfony003parser>phpunit tests\AppBundle\InvestorsParser\Local\ParserLocalTest.php