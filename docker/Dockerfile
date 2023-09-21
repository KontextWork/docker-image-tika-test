FROM apache/tika:2.9.0.0-full

COPY config/tika-config.xml /tika-config.xml
COPY testfiles/dummy.pdf /files/dummy.pdf

ENTRYPOINT [ "/bin/sh", "-c", "exec java -cp \"/tika-server-standard-${TIKA_VERSION}.jar:/tika-extras/*\" org.apache.tika.server.core.TikaServerCli -h 0.0.0.0 $0 $@ -c /tika-config.xml"]