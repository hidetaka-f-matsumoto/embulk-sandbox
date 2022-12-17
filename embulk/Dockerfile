FROM openjdk:8-slim

RUN apt update && apt install -y wget

RUN wget -q https://dl.embulk.org/embulk-latest.jar -O /bin/embulk \
    && chmod +x /bin/embulk

RUN embulk gem install \
    embulk-input-postgresql

WORKDIR /app
COPY . .

ENTRYPOINT ["bash"]
