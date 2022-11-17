FROM docker.graphaware.com/mirror/neo4j:5.1.0-enterprise

COPY plugin/*.jar /var/lib/neo4j/labs/myproc.jar

RUN mv /startup/neo4jlabs-plugins.json /startup/neo4jlabs-plugins-old.json
RUN cat /startup/neo4jlabs-plugins-old.json | jq '. += {"myproc": {"location":"/var/lib/neo4j/labs/myproc.jar","properties":{"dbms.security.procedures.unrestricted":"myproc.*"}}}' > /startup/neo4jlabs-plugins.json