1  apt-get update
2  apt-get install curl -y
3  curl -sL https://deb.nodesource.com/setup_10.x | bash
4  apt-get install nodejs -y
5  cd opt
6  mkdir node-app
7  cd node-app
8  echo 'console.log("nodejsapp from ubuntu...");' > index.js
10  node index.js