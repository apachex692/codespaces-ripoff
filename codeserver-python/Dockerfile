FROM lscr.io/linuxserver/code-server:latest

RUN \
  apt-get update && \
  apt-get install -y python3 python3-virtualenv tree && \
  apt-get autoremove -y --purge && apt-get clean && \
  mkdir -p /config/data/User/ && \
  rm -r -f \
    /config/* \
    /tmp/* \
    /var/lib/apt/lists/* \
    /var/tmp/*

COPY ../vscode/settings.json /config/data/User/settings.json

EXPOSE 8443
