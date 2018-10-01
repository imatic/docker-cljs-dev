FROM imatic/docker-node-dev:8

ENV JOKER_VERSION="0.10.0"

RUN apt-get update && \
    apt-get install -y unzip && \
    # lein
    curl --output /usr/local/bin/lein https://raw.githubusercontent.com/technomancy/leiningen/stable/bin/lein && \
    chmod +x /usr/local/bin/lein && \
    lein && \
    # joker
    wget -O /opt/joker.zip https://github.com/candid82/joker/releases/download/v${JOKER_VERSION}/joker-${JOKER_VERSION}-linux-amd64.zip && \
    mkdir -p /opt/joker && \
    unzip /opt/joker.zip -d /opt/joker && \
    mv /opt/joker/joker /usr/local/bin/joker && \
    # cleanup
    rm -rf /var/lib/apt/lists/*
