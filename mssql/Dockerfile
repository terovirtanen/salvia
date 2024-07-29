# https://hub.docker.com/_/microsoft-mssql-server
FROM mcr.microsoft.com/mssql/server:2019-CU16-ubuntu-20.04

WORKDIR /usr/src

# Copy files over
COPY . /usr/src


RUN mkdir -p  /var/opt/mssql/data && chgrp -R 0 /var/opt/mssql/data && chmod g+w -R /var/opt/mssql/data
RUN mkdir -p  /var/opt/mssql/log && chgrp -R 0 /var/opt/mssql/log && chmod g+w -R /var/opt/mssql/log

ENTRYPOINT /bin/bash ./entrypoint.sh

