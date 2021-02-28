# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

RUN chgrp -R 0 /var/log/httpd && \
    chmod -R g=u /var/log/httpd

USER 1001
