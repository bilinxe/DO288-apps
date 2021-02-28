# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.openshift.expose-services="8080:http"
      io.openshift.tags="httpd, apache"
      io.k8s.description="Child image"
      io.k8s.display-name="Apache HTTP Server"

ENV DIRS /var/log/httpd /var/run/httpd

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf && \
    chgrp -R 0 $DIRS && \
    chmod -R g=u $DIRS

USER 1001
