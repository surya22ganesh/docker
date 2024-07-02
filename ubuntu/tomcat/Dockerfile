FROM ubuntu
RUN apt update -y
RUN apt install docker.io -y
RUN apt install default-jdk -y
ADD https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.100/bin/apache-tomcat-8.5.100.tar.gz .
RUN tar -xvzf apache-tomcat-8.5.100.tar.gz
COPY SampleWebApp.war .
COPY SampleWebApp.war apache-tomcat-8.5.100/webapps/
EXPOSE 8080
CMD ["apache-tomcat-8.5.100/bin/catalina.sh","run"]