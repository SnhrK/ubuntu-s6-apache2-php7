## ubuntu-s6-apache2-php7(-with-cron)

run php server under Apache httpd + mod_php and crond.

This image built based on [mobingidocker/dockerimage-boilerplate](https://github.com/mobingidocker/dockerimage-boilerplate).

- code: /var/www/html
- DocumentRoot: /var/www/html/public


```
$ docker build -f 7.2/Dockerfile -t ubuntu-apache2-php7:7.2 .
```

Run like under the alm-agent.

```
$ git clone https://github.com/mobingilabs/default-site-php -b dir_public test/code
$ docker run --rm \
  -v `pwd`/test/code:/var/www/html/ \
  -v `pwd`/test/code/mobingi-init.sh:/tmp/init/init.sh \
  -p 8080:80 ubuntu-apache2-php7:7.2
```

