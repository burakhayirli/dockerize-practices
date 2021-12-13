FROM php:7.4-fpm

RUN apt update && apt install -y curl nano

RUN docker-php-ext-install pdo

#RUN groupadd -g BURAKHAYIRLIDEV www
#RUN useradd -u BURAKHAYIRLIDEV -ms /bin/bash -g www www

#IMAGE'IN İÇERİSİNDEKİ PROJE DİZİNİ
#COPY İLE PROJECT DOSYALARINI BU DİZİNE KOPYALIYORUZ.
WORKDIR /e/docker_folder/www/
COPY --chown=www:www . /e/docker_folder/www

#USER www

#DIŞARIYA PORT AÇMAK İÇİN
EXPOSE 9000
CMD ["php-fpm"]
