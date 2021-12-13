FROM node:14-slim
WORKDIR /opt/node-server
#COPY app.js .
COPY app/. .
RUN npm install 
#EXPOSE 3000
CMD ["node","app.js"]