# Ansible Role: php5

PHP is a popular general-purpose scripting language that is especially suited to web development.

[https://secure.php.net/](https://secure.php.net/)

# Role Variables

```
php_root: /etc/php/5.6
```
root of php

```
date_timezone: Asia/Taipei
```

Timezone

```
post_max_size: 8M
```

maximum size of http post

```
fpm_listen: /var/run/php5-fpm.sock
```

fpm_listen path

```
php5_packages: []
```

php5 package to install, for example:

* - php5.6-cli

# Example Playbook

```
- hosts: server
  vars:
    php_root: /etc/php/5.6
    date_timezone: Asia/Taipei
    post_max_size: 20M
    fpm_listen: /var/run/php5-fpm.sock
    php5_packages:
      - php5.6-cli
      - php5.6-common
      - php5.6-curl
      - php5.6-dev
      - php5.6-fpm
      - php5.6-gd
      - php5.6-json
      - php5.6-readline
      - php5.6-xml
      - php-pear
  roles:
    - { role: honomoa.php5 }
```

# License
CC BY-SA 3.0
