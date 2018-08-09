FROM jboss/wildfly:latest
RUN /opt/jboss/wildfly/bin/add-user.sh admin Admin#70365 --silent
ADD YOUR_WAR_FILE.war /opt/jboss/wildfly/standalone/deployments/
ADD YOUR_STANDALONE_CONF.xml /opt/jboss/wildfly/standalone/configuration/
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0"]
EXPOSE 8080