FROM tomcat:8.5-jdk11-openjdk

#Update the OS
RUN apt-get update

#Install net tool
RUN apt-get install net-tools -y

#Clean Tomcat webapps folder
RUN rm -rf /usr/local/tomcat/webapps/*
 
COPY project /usr/local/tomcat/webapps/

#Copy Tomcat conf with open AJP port and ip address to any
COPY server.xml /usr/local/tomcat/conf/server.xml

EXPOSE 8009

CMD ["catalina.sh", "run"]