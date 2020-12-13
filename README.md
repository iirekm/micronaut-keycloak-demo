# Micronaut + KeyCloak Demo

## Running 

- Run in terminal: `docker run --publish 8081:8080 -e KEYCLOAK_USER=test -e KEYCLOAK_PASSWORD=test jboss/keycloak:11.0.3`
- Go to http://localhost:8081/auth/admin/master/console/
- Create a client with `Access Type` set to `confidential` and `Redirect URL` set to `http://localhost:8080/*`
- Click `Save` and copy `Client ID` and `Credentials > Secret`
- Run: `./gradlew assemble`
- Run: `OAUTH_CLIENT_ID=<your client id> OAUTH_CLIENT_SECRET=<your client secret> java -jar build/libs/micronaut-keycloak-0.1-all.jar`
- The app is running at http://localhost:8080
