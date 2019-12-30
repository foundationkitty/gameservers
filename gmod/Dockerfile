FROM debian

RUN \
apt-get update && \
apt-get dist-upgrade -y && \
apt install lib32gcc1 -y --no-install-reccomends && \
apt autoremove -y && \
apt autoclean -y && \
rm -rf /var/lib/apt/lists/*

CMD \
/steamcmd/steamcmd.sh +login anonymous +force_install_dir /gmod +app_update 4020 validate +quit && /bin/sh -c '/gmod/srcds_run -game garrysmod +maxplayers "$PLAYERS" +map "$MAP" -port "$PORT"'

WORKDIR /gmod
