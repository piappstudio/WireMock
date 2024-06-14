# Configuring Wiremock

Use this wiremock to project to configure your mock data for various endpoints and address the intermediate 
gap between server vs client during the development process.

## To START Server
1. Make sure java is configured in your command prompt properly.
2. Open command terminal and execute below command 

   java -jar wiremock-standalone-3.6.0.jar --port 9191 --verbose --global-response-templating --jetty-header-buffer-size 16384
3. Kill the command prompt properly to stop the server


## To detect existing listening port and kill it
Assuming 9191 is the listening port we used.
### At Windows Machine
1. netstat -ano | findstr :9191
2. taskkill /PID 152 /F
