FROM  cimg/php:7.3.31

RUN   curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash - \
      && sudo apt-get update && sudo apt-get install -y build-essential apt-transport-https curl ca-certificates gnupg2 apt-utils nodejs libpng-dev libcurl4-openssl-dev pkg-config libssl-dev python3 python3-venv python3-pip\
      && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - \
      && echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list \
      && sudo apt-get update && sudo apt-get install -y yarn ruby-sass locales-all \
      && sudo pecl install mongodb-1.9.0 \
      && php --ini && php --version \
      && echo "extension=mongodb.so" | sudo tee -a /etc/php/7.3/cli/php.ini \
      && sudo composer self-update
