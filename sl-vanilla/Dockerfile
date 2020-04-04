FROM mono:slim

RUN apt update && \
apt dist-upgrade -y && \
apt install lib32gcc1 -y --no-install-reccomends && \

apt autoremove -y && \
apt autoclean -y && \
rm -rf /var/lib/apt/lists/*

CMD \
/steamcmd/steamcmd +login anonymous +force_install_dir /scpsl +app_update 996560 validate -beta Linux +quit && /scpsl/LocalAdmin "$SERVER_PORT"

WORKDIR /scpsl
