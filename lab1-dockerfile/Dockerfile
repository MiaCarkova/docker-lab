FROM ubuntu

ENV DEBIAN_FRONTEND=noninteractive

# установка пакетов
RUN apt-get update 
RUN apt-get install apache2 -y
RUN apt-get install php libapache2-mod-php -y

RUN echo "ServerName localhost" | tee /etc/apache2/conf-available/servername.conf
RUN a2enconf servername
# конфигурации
# RUN rm -f /etc/nginx/sites-enabled//default
# ADD ./cfg/mysite /etc/nginx/sites-available/mysite
# RUN ln -s /etc/nginx/sites-available/mysite /etc/nginx/sites-enabled/mysite

EXPOSE 80

CMD apachectl -D FOREGROUND
