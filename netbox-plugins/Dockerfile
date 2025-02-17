ARG VERSION=v4.2.2  # renovate: datasource=docker depName=ghcr.io/netbox-community/netbox
FROM ghcr.io/netbox-community/netbox:${VERSION}

COPY requirements.txt /requirements.txt

RUN /usr/local/bin/uv pip --no-cache-dir install -U 'pip==25.0.1' \
    && /usr/local/bin/uv pip --no-cache-dir install -r /requirements.txt

LABEL "org.opencontainers.image.documentation"="https://regiocloud.github.io/docs" \
      "org.opencontainers.image.licenses"="ASL 2.0" \
      "org.opencontainers.image.source"="https://github.com/regiocloud/container-images" \
      "org.opencontainers.image.url"="https://ghcr.io/regiocloud/netbox-plugins" \
      "org.opencontainers.image.vendor"="23Technologies GmbH"
