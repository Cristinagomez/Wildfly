FROM quay.io/wildfly/wildfly
# docker run -p 8080:8080 -p 9990:9990 -it quay.io/wildfly/wildfly /opt/jboss/wildfly/bin/standalone.sh -b 0.0.0.0 -bmanagement 0.0.0.0
EXPOSE 8080/tcp
EXPOSE 9990/tcp
COPY demo-0.0.1-SNAPSHOT.war /opt/jboss/wildfly/standalone/deployments/
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0"]
RUN /opt/jboss/wildfly/bin/add-user.sh -u 'crisuser' -p 'crisuser'

