#Installe alpine:3.4
FROM alpine:3.4

#Lance les commandes : ici met à jour nginx et php5 puis créé ensuite un dossier /run/nginx.
RUN apk --update add nginx php5-fpm && \
    mkdir -p /run/nginx

#Créé le fichier suivant .
ADD www /www
#Puis celui la ..
ADD nginx.conf /etc/nginx/
#Puis celui la ...
ADD php-fpm.conf /etc/php5/php-fpm.conf
#Et encore celui la ....  ＼（＾○＾）人（＾○＾）／
ADD run.sh /run.sh

#Créé la variable d'environnement suivante
ENV LISTEN_PORT=80

#Le container écoutera donc sur le port 80
EXPOSE 80

#Commande par défaut à éxécuter pour lancer le container
CMD /run.sh
