
FROM tomcat:10.1-jdk17-temurin

# 2. Remove default Tomcat sample apps
RUN rm -rf /usr/local/tomcat/webapps/*

# 3. Copy the compiled .war file built by Jenkins into Tomcat's webapps folder as ROOT.war
COPY target/*.war /usr/local/tomcat/webapps/ROOT.war

# 4. Expose port 8080 (Tomcat's default port)
EXPOSE 8080

# 5. Start Tomcat server
CMD ["catalina.sh", "run"]
