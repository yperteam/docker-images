FROM quay.io/keycloak/keycloak:20.0.1 as builder

# Enable health and metrics support
ENV KC_HEALTH_ENABLED=true
ENV KC_METRICS_ENABLED=true

# Add Yper theme
# COPY ./themes/<yourThemeName>/ /opt/keycloak/themes/<yourThemeName>/

# Configure a database vendor
ENV KC_DB=mariadb

RUN /opt/keycloak/bin/kc.sh build

FROM quay.io/keycloak/keycloak:20.0.1
COPY --from=builder /opt/keycloak/ /opt/keycloak/
ENTRYPOINT ["/opt/keycloak/bin/kc.sh"]
