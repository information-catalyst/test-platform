FROM jboss/keycloak:6.0.1

USER jboss

RUN sed -i -e 's/<web-context>auth<\/web-context>/<web-context>aim\/auth<\/web-context>/' $JBOSS_HOME/standalone/configuration/standalone.xml
RUN sed -i -e 's/<web-context>auth<\/web-context>/<web-context>aim\/auth<\/web-context>/' $JBOSS_HOME/standalone/configuration/standalone-ha.xml


COPY vf-OS-realm.json .

LABEL vf-OS=true
LABEL vf-OS-platform=true
LABEL vf-OS.backendUri="/aim/auth/"
