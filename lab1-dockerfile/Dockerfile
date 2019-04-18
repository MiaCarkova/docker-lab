FROM ubuntu

ENV DEBIAN_FRONTEND=noninteractive

# установка пакетов
RUN apt-get update 
RUN apt-get install apache2 -y
RUN apt-get install php libapache2-mod-php -y

# конфигурации
RUN echo "ServerName localhost" | tee /etc/apache2/conf-available/servername.conf
RUN a2enconf servername

EXPOSE 80

CMD apachectl -D FOREGROUND
