FROM registry.access.redhat.com/ubi8/nginx-120

# Add application sources
ADD nginx.conf /etc/nginx/
ADD nginx-default-cfg/*.conf /opt/app-root/etc/nginx.default.d/
ADD nginx-cfg/*.conf /opt/app-root/etc/nginx.d/
ADD *.html ./
ADD scripts/* /opt/app-root/bin/

#Needed for execute chgrp and chmod
USER root

CMD /opt/app-root/bin/run.sh

