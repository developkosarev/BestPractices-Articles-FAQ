## Regular Expression

## Contents

Тестирование регулярных выражений 
https://regex101.com/

## PHP examples

```$pattern = '/[0-9]/';```  //паттерн на поиск числа в любом месте строки,в данном случае везде найдется (все валидное)  
```$pattern = '/^[0-9]/';``` //галочка символизирует начало строки, после начала  должны идти числа от 0 до 9 (а109, a109c невалидны)  
```$pattern = '/^[0-9]$/';``` //$заканчиваться числом, но только строка из одного символа (1,2,3 валидно 222 уже не валидно)  
```$pattern = '/^[0-9][0-9][0-9]$/';``` //111,222,333 валидно 4444 не валидно  
```$pattern = '/^[0-9][a][0-9]$/';``` //1a1 валидно  
```$pattern = '/^[0-9]+$/';``` //+ указывает любое количество допустимых значений (11111111, 222, 333 все валидно)  
```$pattern = '/^[0-9]*$/';``` //* аналог + но и пустая строка валидна {0,}  
```$pattern = '/^[0-9]{2,5}$/';``` //длинна числа может быть от 2 до 5 (22, 55555 валидно, 666666 уже не валидно)  
```$pattern = '/^[0-9]*$/';``` //{0,} От 0 до бесконечности  
```$pattern = '/^[0-9]+$/';``` //{1,} От 1 до бесконечности  
```$pattern = '/^[0-9]?$/';``` //{,1} одно повторение символа  
```$pattern = '/^[0-9a-z\-\.]+$/';``` // от 0 до z и дефис и точка, \ экранируем дефиз и точку  
```$pattern = '/^[0-9a-zA-Z]+$/';``` //и большие буквы  
```$pattern = '/^[0-9a-z]+$/i';``` //i отключает регистр  
```$pattern = '/^[^0-9]+$/';``` // ^ Исключаем все цифры  
```$pattern = '/^(dev[0-9]\.)?sunday\.(de|local)\(:[0-9][0-9][0-9][0-9])?(\/fr\/).*';``` //(:[0-9][0-9][0-9][0-9])? ?делает группу не обязательной (валидно dev1.sunday.de:8080/fr/ и dev1.sunday.de/fr/) 

```php
$arr = ['109', 'a109', 'a109c', '']
foreach($arr as $item){
    $res = preg_match($pattern, $item); // возвращает 1 или 0
    if ($res) {
        echo 'Valid';
    } else {
        echo 'Fall';
    }
}
```