# Deploy a Sample JAVA web application on tomcat application server - Ubuntu/Debian

[![Watch the video](https://img.youtube.com/vi/Vi56xFX10iI&t=4s/0.jpg)](https://www.youtube.com/watch?v=Vi56xFX10iI&t=4s)


1. Provision a Linux - Debian 12 virual machine. (GCP Compute Engine). Use EC2 for AWS, Virtual Machine for Microsoft Azure.

2. Download Tomcat's binary by visiting https://tomcat.apache.org/ page.

3. Extract the archived Tomcat's file by using zip.

4. Install JAVA (openjdk).

5. Locate JAVA_HOME JDK's path and set the JAVA_HOME environment variable permanently in .bashrc configuration file.

6. Check for executable permissions on shell scripts available in binaries & provide through chmod command.

7. Invoke the startup script. Tomcat should be started at this point.

8. Verify it by running the process and curl commands.

9. Fetch the public IP of the VM & traverse to the browser for accessing the tomcat server's home page. Note that tomcat runs on a default port 8080.

10. Connection may get timed out if 8080 port is not open. Add a firewall rule to the network by limiting it to specific source IP range.

11. Tomcat server's home page should be accessible.

12. Use wget or curl command for the link https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/sample.war to download the sample java application - hello world into the compute instance.

13. Move the app into apache-tomcat's webapp directory. This should extract the artifacts.

14. Access the sample application through http://PUBLIC-IP:8080/sample.

15. To deploy the sample application with the root context, we need to shutdown the server by invoking the shutdown script or catalina script with stop argument. Once the Tomcat server is stopped, remove the ROOT, SAMPLE directories from apache-tomcat's webapp directory & rename sample.war to ROOT.war. 

16. Finally, Restart the server & the hello world application should be accessible via http://PUBLIC-IP:8080/.
