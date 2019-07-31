FROM node

RUN \
apt-get update && \
apt-get dist-upgrade -y && \
apt-get install unzip wget -y && \
npm install pm2 -g && \
mkdir /pm2

WORKDIR /pm2

CMD ["pm2-runtime", "/pm2/$NODEFILE.js"]
