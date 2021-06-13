FROM influxdb:2.0.7

HEALTHCHECK --interval=5s --timeout=5s CMD curl -f http://localhost:8086 || exit 1