# Docker-base stack
Containerized tech stack using Docker. docker-compose.yml will default this to drupal project 8.

## Introduction

Base-Container-Architecture is a set of docker images optimized for Drupal. Use docker-compose.yml file from this repository to spin up local environment on Linux, Mac OS X and Windows. 

## Stack

[wodby/drupal-nginx]: https://github.com/wodby/drupal-nginx
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/drupal]: https://github.com/wodby/drupal
[wodby/drupal-php]: https://github.com/wodby/drupal-php
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/redis]: https://github.com/wodby/redis
[wodby/drupal-varnish]: https://github.com/wodby/drupal-varnish
[wodby/drupal-solr]: https://github.com/wodby/drupal-solr
[wodby/drupal-node]: https://github.com/wodby/drupal-node
[wodby/memcached]: https://github.com/wodby/memcached
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[wodby/rsyslog]: https://hub.docker.com/r/wodby/rsyslog
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[wodby/adminer]: https://hub.docker.com/r/wodby/adminer
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/portainer/portainer
[_/node]: https://hub.docker.com/_/node
[_/traefik]: https://hub.docker.com/_/traefik

The Drupal stack consist of the following containers:

| Container  | Versions           | Service name | Image                              | Enabled by default |
| ---------- | ------------------ | ------------ | ---------------------------------- | ------------------ |
| Nginx      | 1.13, 1.12         | nginx        | [wodby/drupal-nginx]               | ✓                  |
| Apache     | 2.4                | apache       | [wodby/php-apache]                 |                    |
| Drupal     | 8, 7, 6            | php          | [wodby/drupal]                     | ✓                  |
| PHP        | 7.1, 7.0, 5.6, 5.3 | php          | [wodby/drupal-php]                 |                    |
| MariaDB    | 10.1               | mariadb      | [wodby/mariadb]                    | ✓                  |
| Redis      | 3.2, 4.0           | redis        | [wodby/redis]                      |                    |
| Varnish    | 4.1                | varnish      | [wodby/drupal-varnish]             |                    |
| Solr       | 6.6-6.3, 5.5, 5.4  | solr         | [wodby/drupal-solr]                |                    |
| Node.js    | 1.0                | nodejs       | [wodby/drupal-node]                |                    |
| Memcached  | 1.4                | memcached    | [wodby/memcached]                  |                    |
| Webgrind   | 1.5                | webgrind     | [wodby/webgrind]                   |                    |
| Blackfire  | latest             | blackfire    | [blackfire/blackfire]              |                    |
| Rsyslog    | latest             | rsyslog      | [wodby/rsyslog]                    |                    |
| AthenaPDF  | 2.10.0             | athenapdf    | [arachnysdocker/athenapdf-service] |                    |
| Mailhog    | latest             | mailhog      | [mailhog/mailhog]                  | ✓                  |
| Adminer    | 4.3                | adminer      | [wodby/adminer]                    |                    |
| phpMyAdmin | latest             | pma          | [phpmyadmin/phpmyadmin]            |                    |
| Node       | latest             | node         | [_/node]                           |                    |
| Portainer  | latest             | portainer    | [portainer/portainer]              | ✓                  |
| Traefik    | latest             | traefik      | [_/traefik]                        | ✓                  |

## License

This project is licensed under the MIT open source license.
