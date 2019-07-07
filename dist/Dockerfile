FROM ubuntu
RUN apt-get -y update \
    && apt-get -y upgrade \
    && apt-get install -y apache2 \
    && apt-get install nano \
    && apt-get -y install mysql-server \
    && service mysql start \
    && chown -R mysql:mysql /var/lib/mysql /var/run/mysqld \
    && apt-get install -y nodejs \
    && rm /var/www/html/index.html \
    && service apache2 start \


    COPY . /var/www/html

EXPOSE 80