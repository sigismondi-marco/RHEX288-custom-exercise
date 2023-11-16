FROM registry.access.redhat.com/ubi8/nginx-120

# Add application sources
ADD nginx.conf "${NGINX_CONF_PATH}"
ADD nginx-default-cfg/*.conf "${NGINX_DEFAULT_CONF_PATH}"
ADD nginx-cfg/*.conf "${NGINX_CONFIGURATION_PATH}"
ADD *.html ./
ADD scripts/* /opt/app-root/src/

CMD /opt/app-root/src/run.sh

