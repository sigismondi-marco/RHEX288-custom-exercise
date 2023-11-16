FROM   registry.access.redhat.com/ubi8/ubi:8.0

MAINTAINER   Marco Sigismondi <sigismondi.marco@gmail.com>

RUN   useradd custom && \
      mkdir -p /opt/app-root/bin

COPY  ./scripts/run.sh /opt/app-root/bin/

RUN   chown -R 0 /opt/app-root && \
      chmod -R g=u /opt/app-root

EXPOSE 8080

CMD   /opt/app-root/bin/run.sh
