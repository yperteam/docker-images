FROM  cimg/python:3.7.12

RUN   sudo apt-get update \
      && sudo apt-get install locales-all -y

RUN  wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add - \
      && echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list \
      && sudo apt-get update \
      && sudo apt-get install mongodb-org-tools -y

RUN   sudo apt-get update \
      && sudo apt-get install pipenv -y
      
RUN   sudo apt-get clean
