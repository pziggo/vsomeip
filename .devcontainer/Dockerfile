FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

ARG TIPI_VERSION=v0.0.55

RUN curl -sSLO https://github.com/tipi-build/cli/releases/download/${TIPI_VERSION}/tipi-${TIPI_VERSION}-linux-x86_64.zip && \
    unzip tipi-$TIPI_VERSION-linux-x86_64.zip -d /usr/local -x LICENSE && \
    rm tipi-$TIPI_VERSION-linux-x86_64.zip && \
    chmod 0755 /usr/local/bin/tipi && \
    mkdir /usr/local/share/.tipi && \
    /usr/local/bin/tipi --dont-upgrade run echo "tipi version ${TIPI_VERSION} installed" && \
    chown -R vscode:vscode /usr/local/share/.tipi