# Configuring Wiremock

Utilize this Wiremock project to configure mock data for various endpoints, bridging the gap between server and client during development.

## Setup Postman
1. Install postman and import workspace file "WireMock-BiggBoss.postman_collection.json" available in the root folder.

## Starting the Server
1. Ensure Java is properly configured in your command prompt.
2. Open a command terminal and execute the following command:

   ```sh
   java -jar wiremock-standalone-3.6.0.jar --port 9191 --verbose --global-response-templating --jetty-header-buffer-size 16384
   ```
3. Properly close the command prompt to stop the server.

## Detecting and Terminating an Existing Listening Port
Assuming the listening port used is 9191.

### On Windows
1. Run the command:
   ```sh
   netstat -ano | findstr :9191
   ```
2. Terminate the process with: Here, 152 is pid returned above netstat command
   ```sh
   taskkill /PID 152 /F
   ```
