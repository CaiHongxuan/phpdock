# phpdock
The PHP development for Docker.

# 包含了哪些内容
- Nginx（1.17.9）
- Mysql（5.6.40）
- MongoDB（3.4）
- PHP-FPM（5.4、5.5、5.6、7.3）
- Rdis（2.6、2.8、3.2）

# 运行
安装docker后，在根目录（docker-compose.yml文件所在目录）执行：
```
docker-compose up -d
```
docker-compose.yml文件默认挂载的目录是`D:\Docker`，记得替换成自己实际的目录。

# 目录结构
```
logs  --存放日志文件
    nginx  --存放nginx日志
mysql --存放mysql相关信息
    conf.d  --存放mysql配置文件
        mysql.cnf  --配置文件
    data  --存放mysql数据
nginx  --存放nginx相关配置
    conf.d  --存放虚拟域名配置
        default.conf --默认配置
    nginx.conf  --nginx配置文件
php-fpm54  --存放5.4版本的phpfpm相关文件
    conf.d  --存放扩展配置
        docker-php-ext-bcmath.ini
        ...
    php.ini  --phpfpm配置文件
php-fpm55
    conf.d
        docker-php-ext-bcmath.ini
        ...
    php.ini
php-fpm56
    conf.d
        docker-php-ext-bcmath.ini
        ...
    php.ini
php-fpm73
    conf.d
        docker-php-ext-bcmath.ini
        ...
    php.ini
redis26  --存放2.6版本的redis相关文件
    data  -- 存放redis持久化文件。如：dump.rdb、appendonly.aof
    redis.conf  --redis配置文件
redis28
    data
    redis.conf
redis32
    data
    redis.conf
www  --存放代码
docker-compose.yml

```