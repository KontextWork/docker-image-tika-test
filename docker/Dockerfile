FROM apache/tika:2.9.0.0-full

COPY config/tika-config.xml /tika-config.xml
COPY testfiles/dummy.pdf /files/dummy.pdf

LABEL org.opencontainers.image.source = "https://github.com/KontextWork/docker-image-tika-test"

EXPOSE 9998
ENTRYPOINT [ "/bin/sh", "-c", "exec java -cp \"/tika-server-standard-${TIKA_VERSION}.jar:/tika-extras/*\" org.apache.tika.server.core.TikaServerCli -h 0.0.0.0 $0 $@ -c /tika-config.xml"]