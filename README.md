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

  # 2) JETTY STRUCTURE
         
         
   
 
 
 ![123](https://user-images.githubusercontent.com/79251268/131486655-06a0781c-f544-48cc-8dd6-4f76fb09e4f1.png)
 
 
 
 
 # 3) USING WAR (Deploying web application by copying WAR)
* To deploy a web application to a Jetty server, transfer the WAR file into $JETTY_HOME/webapps directory.
* Navigating into $JETTY HOME and performing the command will start the server:
          
    ```java -jar start.jar```
          
* /Jetty-app context will host our new app.
        
        
        
![6](https://user-images.githubusercontent.com/79251268/131491606-cae8f964-d4d8-43ff-b0be-c5591da6b320.png)
        
        
        
        
        
        
        
* Hello world! should appear on the screen if we navigate to the URL given below in the web browser.
        
   ```http://localhost:8080/jetty-app```
          
          
          
          
          
          
          
![7](https://user-images.githubusercontent.com/79251268/131492204-0901dc8b-3c27-4efb-92ef-a937c38ccd67.png)

 # 4) USING JETTY MAVEN PLUGIN (Deploying web application by using jetty maven plugin)
  * As we build Java web applications, the jetty Maven plugin allows us to perform rapid testing and iteration.
  * Adding the plugin to pom.xml is all that's required to deploy and run applications with it:

    ```<plugin>
    <groupId>org.eclipse.jetty</groupId>
    <artifactId>jetty-maven-plugin</artifactId>
    <version>9.3.11.v20160721</version>
</plugin>```
  * After adding the plugin, we navigate to the root of our app and run the following command:
 
     ```mvn jetty:run```
  
![8](https://user-images.githubusercontent.com/79251268/131664966-876584b8-065e-44c9-ab72-1205a7d2b6f9.png)

![9](https://user-images.githubusercontent.com/79251268/131665633-d3ecdc24-b201-482b-93ff-3cda8796f509.png)


  
 * The plugin deploys the app to a new jetty instance created by this command. We can get to it by typing the URL given below:
  
    ```http://localhost:8080```
  
 ![10](https://user-images.githubusercontent.com/79251268/131665972-2acb4cdd-b549-4637-85bc-2d0b30ae839d.png)


        
        
        

 
 
 


   
  
