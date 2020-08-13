ARG BUILD_FROM=homeassistant/armv7-base:3.10
FROM $BUILD_FROM

# Setup base
ARG DEHYDRATED_VERSION
RUN apk add --no-cache openssl \
  && curl -s -o /usr/bin/dehydrated \
    "https://raw.githubusercontent.com/lukas2511/dehydrated/v${DEHYDRATED_VERSION}/dehydrated" \
  && chmod a+x /usr/bin/dehydrated

# Copy data
COPY data/*.sh /

CMD [ "/run.sh" ]
