FROM foundationkitty/gameservers:mono-complete

RUN \
apt-get update && \
apt-get dist-upgrade -y && \
apt-get install -y curl lib32gcc1 xdg-utils && \
mkdir /steamcmd && \
mkdir /smod && \
cd /steamcmd && \
curl -s http://media.steampowered.com/installer/steamcmd_linux.tar.gz | tar -vxz

CMD \
/steamcmd/steamcmd.sh +login anonymous +force_install_dir /smod +app_update 786920 -beta beta validate +quit && /usr/bin/mono /smod/MultiAdmin.exe

WORKDIR /smod
