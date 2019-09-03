FROM debian

RUN \
apt-get update && \
apt-get dist-upgrade -y && \
apt-get install -y curl lib32gcc1 lib32stdc++6 && \
mkdir /steamcmd && \
mkdir /gmod && \
cd /steamcmd && \
curl -s http://media.steampowered.com/installer/steamcmd_linux.tar.gz | tar -vxz && \
useradd -m gmod

CMD \
/steamcmd/steamcmd.sh +login anonymous +force_install_dir /gmod +app_update 237410 validate +quit && /bin/sh -c '/insurgency/srcds_linux -console +map ministry +maxplayers 24 -port 27015'

WORKDIR /gmod

USER gmod
