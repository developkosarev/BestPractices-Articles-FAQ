## Magento 2

### Dependency injection
if you get error in constructor: `Too few arguments to function`
```
bin/magento cache:flush
bin/magento cache:clean
bin/magento setup:upgrade
bin/magento setup:di:compile
```
From magento root directory: ```chmod -R 777 var/*```
