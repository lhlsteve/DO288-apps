# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.openshift.expose-services="8080:http"

LABEL io.k8s.description="A BASIC aPACHE http sERVER CHILD IMAGE, USES onbuild" \
io.k8s.display-name="APACHE http sERVER" \
io.openshift.expose-services="8080:HTTP" \
io.openshift.tags="APACHE, HTTPD"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -r 0 /var/log/httpd /var/run/httpd && \
chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001

