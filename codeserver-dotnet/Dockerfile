FROM lscr.io/linuxserver/code-server:latest

RUN \
  apt-get update && \
  apt-get install -y dotnet-sdk-8.0 && \
  apt-get autoremove -y --purge && apt-get clean && \
  mkdir -p /config/data/User/ && \
  rm -r -f \
    /config/* \
    /tmp/* \
    /var/lib/apt/lists/* \
    /var/tmp/*

COPY ../vscode/settings.json /config/data/User/settings.json

EXPOSE 8443
