ARG FREERADIUS_TAG=3.0.21

FROM freeradius/freeradius-server:$FREERADIUS_TAG

# Ehable check-eap-tls server config to support TLS
RUN ln -s /etc/raddb/sites-available/check-eap-tls /etc/raddb/sites-enabled/check-eap-tls

# Use check-eap-tls server as TLS EAP server
RUN sed '/check-eap-tls/s/#//' /etc/raddb/mods-enabled/eap -i
