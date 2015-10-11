# Jira 7 Service Desk 3
> Version 7.0.0

Docker image of Atlassian Jira 7 Service Desk 3.
## Basic usage
```
docker run --detach --publish 8080:8080 elgreen/jira-service-desk:latest
```
## Reverse Proxy Support
You need to change the `/opt/atlassian/jira/conf/server.xml` file inside the container to include `proxyName` and `proxyPort` attributes. 

Without configuring these attributes, the values returned would reflect the server name and port on which the connection from the proxy server was received, rather than the server name and port to whom the client directed the original request.
