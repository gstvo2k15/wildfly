# wildfly
Repository for wildfly own labs locally, docker and k8s.

## For Domain deployments

1. Execute docker compose lab with:

   `docker compose up -d --force-recreate`

2. Generate silent change for admin user

    `docker exec -it wildfly-dc /opt/jboss/wildfly/bin/add-user.sh admin SuperSecure@2025 -g SuperUser --silent`

3. Verify output

    `docker exec -it wildfly-dc cat /opt/jboss/wildfly/domain/configuration/mgmt-users.properties`
