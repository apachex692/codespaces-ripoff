FROM lscr.io/linuxserver/code-server:latest

RUN \
  apt-get update && \
  sudo apt-get install -y curl tree && \
  curl -fsSL https://deb.nodesource.com/setup_22.x -o ./nodesource_setup.sh && \
  sudo -E bash ./nodesource_setup.sh && \
  sudo apt-get install -y nodejs && \
  apt-get autoremove -y --purge && apt-get clean && \
  mkdir -p /config/data/User/ && \
  rm -r -f \
    /config/* \
    /tmp/* \
    /var/lib/apt/lists/* \
    /var/tmp/* \
    ./nodesource_setup.sh

COPY ../vscode/settings.json /config/data/User/settings.json

EXPOSE 8443
