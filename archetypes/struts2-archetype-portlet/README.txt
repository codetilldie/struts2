INFORMATION
===========
- This is Struts 2's "Portlet" Maven Archetype
- To be used to create a simple portlet that can be deployed as JSR286 portlet.
- There is a maven profile in order to test this portlet on Pluto Portal.
 

USAGE
=====

1- Generate your archetype
- mvn archetype:generate -DartifactId=struts2-portlet-helloworld  -DgroupId=com.mycompany.struts2.portlet -Dversion=1.0.0-SNAPSHOT -DarchetypeGroupId=org.apache.struts -DarchetypeArtifactId=struts2-archetype-portlet -DarchetypeVersion=2.3.8

2- Build your portlet project for Pluto Portal
- cd struts2-portlet-helloworld
- mvn clean package -Ppluto-embedded

3- Download and install Pluto Portal
- cd ..
- curl -v -H "Accept-Encoding: gzip" "http://apache.opensourcemirror.com/portals/pluto/pluto-2.0.3-bundle.zip" > pluto-2.0.3.zip
- unzip pluto-2.0.3.zip -d .

4- Deploy your portlet app
- cp struts2-portlet-helloworld/target/struts2-portlet-helloworld-1.0.0-SNAPSHOT.war pluto-2.0.3/webapps

5- Start Pluto Portal and create a page for your portlet
- ./pluto-2.0.3/bin/startup.sh
- Go to http://localhost:8080/pluto/portal (login: pluto / pwd: pluto)
- Click on "Pluto Admin" (http://localhost:8080/pluto/portal/Pluto%20Admin)
- On "Portal Pages" section : Add page "Struts2"
- On "Portlet Applications" section : select "/struts2-portlet-helloworld" and "HelloPortlet" then click "Add Portlet"

6- Test your portlet app
- Go to your Struts2 page http://localhost:8080/pluto/portal/Struts2 and play with your portlet !!




