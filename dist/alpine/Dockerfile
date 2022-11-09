# Auto-generated via Ansible: edit src/Dockerfiles/all/Dockerfile.j2 instead.

FROM rabbitmq:3.11-alpine

# Labels
# https://github.com/opencontainers/image-spec/blob/main/annotations.md
LABEL "maintainer"="lotyp <lotyp7@gmail.com>"
LABEL "vendor"="wayofdev"
LABEL "org.opencontainers.image.authors"="lotyp <lotyp7@gmail.com>"
LABEL "org.opencontainers.image.url"="https://hub.docker.com/r/wayofdev/rabbitmq"
LABEL "org.opencontainers.image.documentation"="https://github.com/wayofdev/docker-rabbitmq"
LABEL "org.opencontainers.image.source"="https://github.com/wayofdev/docker-rabbitmq"
LABEL "org.opencontainers.image.vendor"="wayofdev"
LABEL "org.opencontainers.image.licenses"="MIT"
LABEL "org.opencontainers.image.ref.name"="3.11-alpine"
LABEL "org.opencontainers.image.title"="rabbitmq-3.11-alpine"
LABEL "org.opencontainers.image.description"="rabbitmq-3.11-alpine"

RUN set -eux; \
    rm -rf /var/cache/apk/* \
    && rm -rf /tmp/* \
    && apk -U upgrade -a \
    && apk add --update --no-cache \
      curl \
      unzip \
    && curl -L -o ./rabbitmq_delayed_message_exchange.zip "https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/releases/download/3.11.1/rabbitmq_delayed_message_exchange-3.11.1.ez" \
        && unzip rabbitmq_delayed_message_exchange.zip \
        && rm -f rabbitmq_delayed_message_exchange.zip \
        && mv rabbitmq_delayed_message_exchange-3.11.1 plugins/ \
        && rabbitmq-plugins enable rabbitmq_delayed_message_exchange \
    && curl -L -o ./rabbitmq_message_timestamp.zip "https://github.com/rabbitmq/rabbitmq-message-timestamp/releases/download/v3.11.1/rabbitmq_message_timestamp-3.11.1.ez" \
        && unzip rabbitmq_message_timestamp.zip \
        && rm -f rabbitmq_message_timestamp.zip \
        && mv rabbitmq_message_timestamp-3.11.1 plugins/ \
        && rabbitmq-plugins enable rabbitmq_message_timestamp \
    && rabbitmq-plugins enable rabbitmq_amqp1_0 \
    && rabbitmq-plugins enable --offline rabbitmq_shovel \
    && apk del -f \
        .build-deps \
        curl \
        unzip
