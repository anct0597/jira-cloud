FROM cptactionhank/atlassian-jira-software:latest

USER root

# Add proxy unpacking to container
COPY "atlassian-agent.jar" /opt/atlassian/jira/
COPY "lib/*" /opt/atlassian/jira/lib
# Set Startup Loading Agent Package
RUN echo 'export CATALINA_OPTS="-javaagent:/opt/atlassian/jira/atlassian-agent.jar ${CATALINA_OPTS}"' >> /opt/atlassian/jira/bin/setenv.sh
