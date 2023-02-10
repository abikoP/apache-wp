FROM wordpress:6.1.1-php8.1


RUN apt-get update \
    && docker-php-ext-install \
      fileinfo \
      mysqli \
      pdo \
      pdo_mysql \
    && apt-get install -y default-mysql-client\
    &&  curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
    && chmod +x wp-cli.phar \
    && mv wp-cli.phar /usr/local/bin/wp \
    && echo "alias wp='wp --allow-root'" >> "${HOME}/.bashrc" \
    && apt-get install nano \
    && apt-get install -y vim

