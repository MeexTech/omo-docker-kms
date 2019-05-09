# 使用
```
~# docker pull xtechcloud/omo-kms
~# docker run --restart=always --name=omo-kms -d xtechcloud/omo-kms
```

# 更改端口 
内部80端口用于http访问，10080端口用于gprc访问

```
~# docker run --restart=always --name=omo-kms -p 10080:80 -p 10088:10080 -d xtechcloud/omo-kms
```

# 使用sqlite

默认使用sqlite，数据库存放于/etc/kms/kms.db,等同于以下方式。

```
~# docker run --restart=always --name=omo-kms -e KMS_DATABASE_DRIVER=sqlite -e KMS_SQLITE_FILEPATH=/etc/kms/kms.db -d xtechcloud/omo-kms
```


# 使用mysql
```
~# docker run --restart=always --name=omo-kms -e KMS_DATABASE_DRIVER=mysql -e KMS_MYSQL_ADDR=127.0.0.1:3306 -e KMS_MYSQL_USER=root -e KMS_MYSQL_PASSWORD=mysql@OMO -e KMS_MYSQL_DATABASE=kms -d xtechcloud/omo-kms
 ```

# API
参考 https://github.com/xtech-cloud/omo-msa-kms
