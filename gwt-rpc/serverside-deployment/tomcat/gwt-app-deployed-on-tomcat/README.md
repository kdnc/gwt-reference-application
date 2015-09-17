## Table of Contents
**[Resource location](#resource-location)**  
**[Overview](#overview)**  
**[Build and Deploy the application](#build-and-deploy-the-application)**  
**[Access the application](#access-the-application)**  

## Resource location
* Git repository - <https://github.com/steinsag/gwt-maven-example>
* Sample video - <https://youtu.be/wszwNLQvZG4>

## Overview
Finally, a working example combining a multi-project maven build together with GWT 2.

This example is based on the GWT webapp created by the [Maven GWT Plugin archetype](http://mojo.codehaus.org/gwt-maven-plugin/user-guide/archetype.html).

I created this example as I was unable to find any **working** example on the net. The example doesn't just compile via Maven, but I was also able to run it in IntelliJ IDEA 11.1 Ultimate.

## Build and Deploy the application

### Running via Maven in GWT Dev Mode
In order to run the example via Maven in GWT Dev Mode, you need to do:

1. Start the web application in Tomcat 7 via Maven
2. Start GWT Dev Mode via Maven
3. Run the application in your browser

To accomplish the first point, issue the following Maven command on a shell:

    mvn clean install
    mvn tomcat7:run-war-only

Your application is now deployed at http://127.0.0.1:8083/parent/.

Now, you need to start GWT Dev Mode. Open a second shell and execute:

    mvn gwt:run -pl web

On success, the GWT Dev Mode window opens. Click *Launch Default Browser* to open it in GWT Dev Mode.

You can now make changes to your client Java code. Changes become immediately available as soon as you reloaded your page in the browser.

## Access the application

The application can be tested with following URLs:     
* http://127.0.0.1:8083/parent/