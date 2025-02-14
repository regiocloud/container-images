ARG VERSION=v4.2.3  # renovate: datasource=docker depName=ghcr.io/netbox-community/netbox
FROM ghcr.io/netbox-community/netbox:${VERSION}

COPY requirements.txt /requirements.txt

RUN /opt/netbox/venv/bin/python3 -m pip --no-cache-dir install -U 'pip==25.0.1' \
    && /opt/netbox/venv/bin/python3 -m pip --no-cache-dir install -r /requirements.txt

LABEL "org.opencontainers.image.documentation"="https://regiocloud.github.io/docs" \
      "org.opencontainers.image.licenses"="ASL 2.0" \
      "org.opencontainers.image.source"="https://github.com/regiocloud/container-images" \
      "org.opencontainers.image.url"="https://ghcr.io/regiocloud/netbox-plugins" \
      "org.opencontainers.image.vendor"="23Technologies GmbH"
