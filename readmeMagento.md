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

### Generate whitelist
```
bin/magento setup:db-declaration:generate-whitelist --module-name=Diko_Enterprise
bin/magento setup:upgrade
```

### Magento 2 xml validation
```
bin/magento dev:urn-catalog:generate .idea/misc.xml
```


### Modules
module-theme responsible for base layouts (1column.xml, 2column-left.xml, .....)