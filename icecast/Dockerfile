# Dockerfile para o Icecast
FROM debian:latest

# Atualiza o sistema e instala dependências
RUN apt-get update && \
    apt-get install -y \
        icecast2 \
        libxml2 \
        libxslt1.1 \
        && apt-get clean

# Verifica se o grupo icecast existe, e se não, cria-o
RUN if ! getent group icecast; then groupadd -r icecast; fi && \
    if ! id -u icecast > /dev/null 2>&1; then useradd -r -g icecast icecast; fi

# Cria diretórios e define permissões
RUN mkdir -p /etc/icecast2 /usr/local/icecast/logs && \
    touch /usr/local/icecast/logs/error.log /usr/local/icecast/logs/access.log && \
    chown -R icecast:icecast /etc/icecast2 /usr/local/icecast/logs

# Copia o arquivo de configuração
COPY icecast.xml /etc/icecast2/icecast.xml

USER icecast
ENTRYPOINT ["icecast2", "-c", "/etc/icecast2/icecast.xml"]

