FROM registry.access.redhat.com/ubi8/nginx-120

# Add application sources
ADD nginx.conf "${NGINX_CONF_PATH}"
ADD nginx-default-cfg/*.conf "${NGINX_DEFAULT_CONF_PATH}"
ADD nginx-cfg/*.conf "${NGINX_CONFIGURATION_PATH}"
ADD *.html ./
ADD scripts/* /opt/app-root/bin/

RUN chgrp -R 0 "${NGINX_CONF_PATH}"/ "${NGINX_DEFAULT_CONF_PATH}"/ "${NGINX_CONFIGURATION_PATH}"/ /opt/app-root/bin/ && \
    chmod -R g=u "${NGINX_CONF_PATH}"/ "${NGINX_DEFAULT_CONF_PATH}"/ "${NGINX_CONFIGURATION_PATH}"/ /opt/app-root/bin/

USER 1001

CMD /opt/app-root/bin/run.sh

