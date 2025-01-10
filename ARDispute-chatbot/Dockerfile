FROM registry.redhat.io/rhel8/httpd-24
USER root
RUN dnf -y update
# Add application sources
COPY . /var/www/html

RUN chgrp -R 0 . && \
    chmod -R g=u .

# The run script uses standard ways to run the application
CMD run-httpd
