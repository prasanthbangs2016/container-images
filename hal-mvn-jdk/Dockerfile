FROM spring-boot-offline-maven

ADD build /usr/local/bin/
ADD run /usr/local/bin/
RUN mkdir /deployments && \
    chown 1001:0 /deployments && \
    chmod a+x /deployments
RUN chmod -R 777 /tmp/artefacts && \
    chown -R 1001:0 /tmp/artefacts
RUN chmod +x /usr/local/bin/run && chmod +x /usr/local/bin/build
CMD ["/usr/local/bin/run"]