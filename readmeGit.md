### **GIT**

##### Настроки git
> git config --global --list *(настройки git)*  
> git config --global user.name 'cfgsoft' *(изменение имени) 'developkosarev'*  
> git config --global user.email 'cfgsoft@yandex.ru' *(изменение email)*  
'develop.kosarev@gmail.com'

##### Инициализация git
> git status  
> git init  

##### Добавление файлов, commit
> git add . *(добавить все файлы в стаждинг эрия)*  
> git commit -m 'first commit' *(Сохраняет изменения с комментрием)*  
> git log  

краткая форма  
>git commit -a -m 'secont commit'  
> git log -p *(выводит изменения в файлах)*  
> git log -2 *(выводит 2 последних commit)*  

##### Работа с удаленным репозиторием
> get remote -v   
*Просмотр удаленный репозиториев*

> git remote add origin https://github.com/cfgsoft/git_test.git  
*Связывает репозиторий с удаленным репозиторием (origin название для примера)*

>git push -u origin master  
*отправка на сервер (имя origin  ветка master ключ -u сохраняет origin master и в следующий раз достаточно написать git push)*

> git clone https://github.com/cfgsoft/git_test.git  
*(клонирует проект на удаленный репозиторий)*  

> git pull, git pull origin  
*(Загрузить изменения из удаленного репозитория)*


#### Ветки
> git branch *(Просмотр веток)*  
> git branch dev *(Создание новой ветки dev)*  
> git checkout dev *(переход в ветку)*

> *//соединить 2 ветки, из своей ветки в мастер *  
> dk@icore7 MINGW64 /c/MyProgram/git/test1 (master)  
> git merge branch2
> *//загрузить изменения из master в свою ветку*  
> git merge master

> *//закоммитить ветки*  
> dk@icore7 MINGW64 /c/MyProgram/git/test1 (master|MERGING)  
> git commit -a -m 'Fixed' [master 7b9d677] Fixed

> git branch -d branch2 *(удалить ветку)*  

> git checkout -b branch3 *(быстрый способ создания веток)*  

> git checkout . *(убрать все изменения)*  
> git clean -fd *(удалить все изменения в точ сисле новые файлы)*  



#### ssh key
[Создание разных ключей для bitbucket https://slicks.name/web-dev/different-ssh-keys-multiple-bitbucket-accounts.html](https://slicks.name/web-dev/different-ssh-keys-multiple-bitbucket-accounts.html)

[Команды по git https://pingvinus.ru/git/1567](https://pingvinus.ru/git/1567)

[Откатить изменения https://server-gu.ru/git-undo-changes/](https://server-gu.ru/git-undo-changes/)

[Объединения coommit Rebase and Squash https://htmlacademy.ru/blog/boost/tools/how-to-squash-commits-and-why-it-is-needed](https://htmlacademy.ru/blog/boost/tools/how-to-squash-commits-and-why-it-is-needed)

> *//проблема с rebase*  
https://stackoverflow.com/questions/18292578/what-does-git-masterrebase-1-1-mean-how-do-i-get-rid-of-it
