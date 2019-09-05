FROM php:7.1-alpine

WORKDIR /tmp

RUN wget https://squizlabs.github.io/PHP_CodeSniffer/phpcs.phar && \
    cp /tmp/phpcs.phar /usr/local/bin/phpcs && \
    chmod +x /usr/local/bin/phpcs
RUN wget https://squizlabs.github.io/PHP_CodeSniffer/phpcbf.phar && \
    cp /tmp/phpcbf.phar /usr/local/bin/phpcbf && \
    chmod +x /usr/local/bin/phpcbf
RUN wget https://phar.phpunit.de/phpcpd.phar && \
    cp /tmp/phpcpd.phar /usr/local/bin/phpcpd && \
    chmod +x /usr/local/bin/phpcpd
COPY --from=phpstan/phpstan:latest /composer/vendor/bin/phpstan /usr/local/bin/phpstan
