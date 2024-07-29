# https://hub.docker.com/_/microsoft-mssql-server
FROM mcr.microsoft.com/mssql/server:2019-CU16-ubuntu-20.04

WORKDIR /usr/src

# Copy files over
COPY . /usr/src


RUN chgrp -R 0 /opt/mssql/bin && chmod g+r -R /opt/mssql/bin
RUN chgrp -R 0 /opt/mssql-tools/bin && chmod g+r -R /opt/mssql-tools/bin

ENTRYPOINT /bin/bash ./entrypoint.sh

