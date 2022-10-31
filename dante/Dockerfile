FROM vimagick/dante

COPY sockd.conf /etc/dante/

ARG SOCKS_USER
ARG SOCKS_PASS

RUN if [ ! -z "$SOCKS_USER" ] && [ ! -z "$SOCKS_USER" ]; then \
        printf "$SOCKS_PASS\n$SOCKS_PASS\n" | adduser $SOCKS_USER; \
        sed -i 's/#socksmethod/socksmethod/g' /etc/dante/sockd.conf; \
    fi
