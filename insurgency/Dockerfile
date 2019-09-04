FROM debian

RUN \
apt-get update && \
apt-get dist-upgrade -y && \
apt-get install -y curl lib32gcc1 lib32stdc++6 lib32z1 && \
mkdir /steamcmd && \
mkdir /insurgency && \
cd /steamcmd && \
curl -s http://media.steampowered.com/installer/steamcmd_linux.tar.gz | tar -vxz && \
useradd -m insurgency

CMD \
/steamcmd/steamcmd.sh +login anonymous +force_install_dir /insurgency +app_update 237410 validate +quit && /bin/sh -c '/insurgency/srcds_run -console +map ministry +maxplayers 24 -port 27015'

WORKDIR /insurgency

USER insurgency
