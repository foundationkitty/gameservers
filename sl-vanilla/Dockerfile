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
/steamcmd/steamcmd +login "$STEAM_USERNAME" "$STEAM_PASSWORD" +force_install_dir /vanilla +app_update 700330 -beta linux validate +quit && /usr/bin/mono /vanilla/MultiAdmin.exe

WORKDIR /vanilla
