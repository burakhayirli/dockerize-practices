FROM node:14-slim
WORKDIR /vue-app
COPY app/ .
#COPY LOCAL, IMAGEIN İÇİ
RUN npm install


#uygulamanın koşacağı sunucuyu yüklüyoruz.
RUN npm install -g live-server

#normalde development modunda olur. build ederek production moduna alıyoruz. ki error logları vs açık olur kapatıyoruz.
#dist klasörü açılır içi doldurulur.
#sunucu sadece dist/ yazılırsa başlar
RUN npm run build

#bu image container olduğundaki kullanacağı port budur diyoruz.
EXPOSE 8080

#live serverda farklı bir port kullanmak istersek bu şekilde parametre olarak gönderiyoruz.
#CMD ["live-server","-p","8090","dist"]

#bir diğer kullanım şekli
#CMD live server -p 8090 dist/

CMD ["live-server","dist"]



