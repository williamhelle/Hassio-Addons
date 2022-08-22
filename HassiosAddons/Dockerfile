ARG BUILD_FROM
# hadolint ignore=DL3006
FROM ${BUILD_FROM}


# Set shell
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN apk update
ENV PYTHONUNBUFFERED=1
RUN apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python
RUN python3 -m ensurepip
RUN pip3 install --no-cache --upgrade pip setuptools
RUN python3 -m pip install -U disnake
RUN python bot.py



# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_REF
ARG BUILD_VERSION

# Labels
LABEL \
    io.hass.name="bagley_bot" \
    io.hass.description="bagley_bot" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Williamhelle <williamhelle@icloud.com>" \
    org.label-schema.description="bagley_bot" \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.name="bagley_bot" \
    org.label-schema.schema-version="1.0" \
    org.label-schema.url="https://github.com/williamhelle/Hassio-Addons" \
    org.label-schema.usage="https://github.com/williamhelle/Hassio-Addons/tree/master/bagley_bot/tree/master/README.md" \
    org.label-schema.vcs-ref=${BUILD_REF} \
    org.label-schema.vcs-url="https://github.com/williamhelle/Hassio-Addons/tree/master/bagley_bot" \
    org.label-schema.vendor="Williamhelle"

