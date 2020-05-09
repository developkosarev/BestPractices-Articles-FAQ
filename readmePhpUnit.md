## PHP Unit

## Contents

Обновление php unit в xampp
https://stackoverrun.com/ru/q/11876059

запуск теста из командной строки
d:\xampp\htdocs\symfony003parser>phpunit tests\AppBundle\Controller\DefaultControllerTest.php
d:\xampp\htdocs\symfony003parser>phpunit tests
d:\xampp\htdocs\symfony003parser>phpunit tests\AppBundle\InvestorsParser\Local\ParserLocalTest.php

1. Unit test
2. Integration test (Как unit test, но с использованием реального соединения с БД)
3. Function test (Команды в браузере)

## setUp
//* This method is called before the first test of this test class is run.
public static function setUpBeforeClass()/* The :void return type declaration that should be here would cause a BC issue */
//* This method is called after the last test of this test class is run.
public static function tearDownAfterClass()/* The :void return type declaration that should be here would cause a BC issue */    
//* This method is called before each test.
protected function setUp()/* The :void return type declaration that should be here would cause a BC issue */
//* This method is called after each test.
protected function tearDown()/* The :void return type declaration that should be here would cause a BC issue */