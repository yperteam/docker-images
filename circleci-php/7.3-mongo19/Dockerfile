FROM  circleci/php:7.3

RUN   curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash - \
      && sudo apt-get update && sudo apt-get install -y build-essential apt-transport-https curl ca-certificates gnupg2 apt-utils nodejs libpng-dev libcurl4-openssl-dev pkg-config libssl-dev \
      && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - \
      && echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list \
      && sudo apt-get update && sudo apt-get upgrade && sudo apt-get install -y yarn ruby-sass locales-all \
      && sudo pecl install mongodb-1.9 \
      && sudo docker-php-ext-enable mongodb-1.9 \
      && sudo docker-php-ext-install gd
