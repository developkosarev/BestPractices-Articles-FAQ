## Parser

## TOR

https://dist.torproject.org/torbrowser/9.0.5/

Скачиваем tor-win32-0.4.2.6.zip
//запускаем с тунелем для http tor.exe --HTTPTunnelPort 8118 (не работает)
https://stackoverflow.com/questions/38950330/tor-is-not-an-http-proxy (настраиваем браузер SOCKS v5  127.0.0.1:9050 )

tor -f 1
tor -f 9052

ControlPort 9051

парсим мемы в питоне
https://habr.com/ru/company/ods/blog/346632/

Парсим сайты PHP тор и струра таблиц
http://rche.ru/2788_parsing-sajtov-v-seti-tor.html

Парсер простой
https://sitkodenis.ru/parser-site-by-php/

Управление tor из PHP
https://github.com/tobozo/php-tor-control-port


//Время смены ip адреса каждые 60 секунд время минимальное время 10 секунд
--MaxCircuitDirtiness 60

start tor.exe --DataDirectory Tor9052 --SocksPort 9052 --ControlPort 9053
start tor.exe --DataDirectory Tor9054 --SocksPort 9054 --ControlPort 9055 