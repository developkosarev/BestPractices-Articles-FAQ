## GIT

git config --global --list (настройки git)
git config --global user.name 'cfgsoft' (изменение имени) 'developkosarev'
git config --global user.email 'cfgsoft@yandex.ru'(изменение email) 'develop.kosarev@gmail.com'

git status
git init

git add . (добавить все файлы в стаждинг эрия)
git commit -m 'first commit' (Сохраняет изменения с комментрием)
git log

git commit -a -m 'secont commit'
git log -p (выводит изменения в файлах)
git log -2 (выводит 2 последних commit)


//Связывает репозиторий с удаленным репозиторием (origin название для примера)
git remote add origin https://github.com/cfgsoft/git_test.git

//отправка на сервер (имя origin  ветка master ключ -u сохраняет origin master и в 
следующий раз достаточно написать git push)
git push -u origin master 
git clone https://github.com/cfgsoft/git_test.git  (клонирует проект на удаленный репозиторий)
git pull (Загрузить изменения из удаленного репозитория)


//Просмотр веток
git branch

//Создание новой ветки dev
git branch dev

//переход в ветку
git checkout dev

//соединить 2 ветки
dk@icore7 MINGW64 /c/MyProgram/git/test1 (master)
$ git merge branch2

//закоммитить ветки
dk@icore7 MINGW64 /c/MyProgram/git/test1 (master|MERGING)
$ git commit -a -m 'Fixed'
[master 7b9d677] Fixed

//удалить ветку
git branch -d branch2


//быстрый способ создания веток
git checkout -b branch3

//Команды по git
https://pingvinus.ru/git/1567


//гтовые карзины на git
https://github.com/topics/shopping-cart


//Откатить изменения
https://server-gu.ru/git-undo-changes/