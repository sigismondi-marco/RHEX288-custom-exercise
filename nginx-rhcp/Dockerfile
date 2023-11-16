FROM registry.access.redhat.com/ubi8/nginx-120

# Add application sources
ADD nginx.conf /etc/nginx/
ADD nginx-default-cfg/*.conf /opt/app-root/etc/nginx.default.d/
ADD nginx-cfg/*.conf /opt/app-root/etc/nginx.d/
ADD *.html ./
ADD scripts/* /opt/app-root/bin/

#Needed for execute chgrp and chmod
USER root

RUN chgrp -R 0 /etc/nginx/ /opt/app-root/etc/nginx.default.d/ /opt/app-root/etc/nginx.d/ /opt/app-root/bin/ && \
    chmod -R g=u /etc/nginx/ /opt/app-root/etc/nginx.default.d/ /opt/app-root/etc/nginx.d/ /opt/app-root/bin/ && \
    chmod 775 /opt/app-root/bin/run.sh /opt/app-root/bin/test.sh

USER 1001

CMD /opt/app-root/bin/run.sh

