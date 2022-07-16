## WordPress

### Files
1. ```sudo chown -R www-data:apache /var/www/html``` Change owner for update  
2. ```sudo chmod 700 id_rsa```
3. ```sudo chmod -R ugo+w or sudo chmod -R ugo-w```
   * u - user; g - group; o - other users;
   * r - чтение; w - запись; x - выполнение; s - выполнение  от имени суперпользователя (дополнительный);
4. ```df -h``` Free space in file system

### Groups
```
$ vi /etc/group
$ sudo groupadd test (add group)
```