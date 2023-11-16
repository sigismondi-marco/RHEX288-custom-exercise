FROM   registry.access.redhat.com/ubi8/ubi:8.0

MAINTAINER   Marco Sigismondi <sigismondi.marco@gmail.com>

RUN   useradd custom && \
      mkdir -p /opt/app-root/bin

COPY  ./scripts/run-app.sh /opt/app-root/bin/

RUN   chown -R custom:custom /opt/app-root && \
      chmod -R 700 /opt/app-root

EXPOSE 80

CMD   /opt/app-root/bin/run.sh
