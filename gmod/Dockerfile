FROM debian

RUN \
apt-get update && \
apt-get dist-upgrade -y && \
apt-get install -y curl lib32gcc1 lib32stdc++6 && \
mkdir /steamcmd && \
mkdir /gmod && \
cd /steamcmd && \
curl -s http://media.steampowered.com/installer/steamcmd_linux.tar.gz | tar -vxz

CMD \
/steamcmd/steamcmd +login "$STEAM_USERNAME" "$STEAM_PASSWORD" +force_install_dir /gmod +app_update 4020 validate +quit && /bin/sh -c '/gmod/srcds_run -game garrysmod +maxplayers $MAXPLAYERS +map $MAP'

WORKDIR /gmod
