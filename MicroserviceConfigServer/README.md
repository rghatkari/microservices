Microservice Components:
1. Microservice config server
2. Eureka discovery Server
3. API Gateway.

Microservice config server: 
    -- Idea is that our program can move settings to an external place so that our application is easily configurable and can even change settings.
    -- The configuration server uses Git repository on GitHub, where we store the configuration files.
    -- spring-cloud-config-server dependency is required.
    -- @EnableConfigServer annotation, with which we instruct Spring Boot to consider this service as a config server application.
    -- In application.properties file, should be the below parameter:
        spring.cloud.config.server.git.uri= < configuration file clone gir repository location >
    -- repo for storing the configuration file - https://github.com/rghatkari/centralProperties
    -- We could also specify use of the repository GitLocally, as follows:
    -- spring.cloud.config.server.git.uri=file://<cloned git repository>
