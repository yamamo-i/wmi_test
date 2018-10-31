FROM prom/prometheus:v2.4.3

COPY docker_entrypoint.sh /bin/docker_entrypoint.sh
USER root
ENTRYPOINT ["/bin/docker_entrypoint.sh"]
CMD        [ "--config.file=/etc/prometheus/prometheus.yml", \
             "--storage.tsdb.path=/prometheus", \
             "--web.console.libraries=/usr/share/prometheus/console_libraries", \
             "--web.console.templates=/usr/share/prometheus/consoles" ]

