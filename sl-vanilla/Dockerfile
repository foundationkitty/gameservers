FROM mono:slim

RUN apt update && \
apt dist-upgrade -y && \
apt install lib32gcc1 -y --no-install-reccomends && \
apt autoremove -y && \
apt autoclean -y && \
rm -rf /var/lib/apt/lists/*

CMD \
/steamcmd/steamcmd +login "$STEAM_USERNAME" "$STEAM_PASSWORD" +force_install_dir /vanilla +app_update 996560 validate -beta Linux +quit && /vanilla/LocalAdmin "$SERVER_PORT"

WORKDIR /vanilla
