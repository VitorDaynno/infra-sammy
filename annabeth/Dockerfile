FROM node:carbon

RUN apt-get update
RUN mkdir /app && \
    git clone https://mathmat@bitbucket.org/vitorDaynno/annabeth.git /app && \
    cd /app && \
    npm install --production && \
    chmod +x start.sh

WORKDIR /app

CMD ["/app/start.sh"]