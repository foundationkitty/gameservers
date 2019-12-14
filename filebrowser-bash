FROM foundationkitty/alpine-bash:latest

RUN \
curl -s https://api.github.com/repos/filebrowser/filebrowser/releases/latest \
  | grep browser_download_url \
  | grep linux-amd64 \
  | cut -d '"' -f 4 \
  | wget -qi - \
  | tar xvf -

CMD /filebrowser
