#image oluşturulurken çalışması gerekenler komutları
FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install curl -y
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install nodejs -y

#eğer WORKDIRı copyden önce alırsak 
# COPY . . olarak kullanılacak
COPY . /opt/node-app/

#bu satırdan sonraki komutların çalışacağı klasör şudur
WORKDIR /opt/node-app
ENV channel=burakhayirli
#container çalışma anında tetiklenecek kısım
#CMD ["node","/opt/node-app/index.js"];
CMD ["node","index.js"];

#terminale geçip bu dizin altında docker build . -t benimimajim komutunu çalıştır.
# -t kullanarak imagea tag veriyoruz.