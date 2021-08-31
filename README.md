# Deploying-Web-Applications-in-Jetty

* We'll start with a quick review of the Jetty web server before moving on to different methods for deploying a WAR file.
# 1) SETUP
   * The very first step to start this is to download the latest version Jetty
   * Let's go to the console, navigate to our desired location, and execute the following command:
   
       ```mvn archetype:generate -DgroupId=com.baeldung -DartifactId=jetty-app -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false```
       
       
       ![2](https://user-images.githubusercontent.com/79251268/131470478-70250680-553e-4aa9-bb07-dfa881bf741a.png)
   
   * This command will generate a complete Java web app in our current location's jetty-app folder. Since, WAR files are involved, so let's head to the root of the project and build it:
   
       ```cd jetty-app```
       
   * Building with Maven:
       
       ```mvn package```
       
        ![3](https://user-images.githubusercontent.com/79251268/131471391-57084846-03ad-433b-b344-a0a84b37ede4.png)
        
        
        ![4](https://user-images.githubusercontent.com/79251268/131471484-c01ee86c-8803-4163-bbe0-c2a55bebdfb7.png)
 
     *  After executing this command jetty-app.war will be created at location jetty-app/target/jetty-app.war.
     
         ![5](https://user-images.githubusercontent.com/79251268/131472010-e7a780b6-381e-4c8e-9d54-e9c07833b909.png)


   
  
