FROM klaemo/couchdb

RUN mkdir -p \
      /opt/couchdb/ && \
    chown -R couchdb.0 \
      /opt/couchdb/ && \
    # Loosen permission bits to avoid problems running container with arbitrary UID
    chmod -R g+rwx \
      /opt/couchdb/

# Copy executable utilities.
COPY bin/ /usr/bin/
COPY docker-entrypoint.sh /

USER couchdb
