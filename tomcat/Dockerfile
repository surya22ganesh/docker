FROM ubuntu
LABEL maintainer="surya"
RUN apt update -y
RUN apt install default-jdk -y
RUN mkdir /opt/tomcat
WORKDIR /opt/tomcat
ADD https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.26/bin/apache-tomcat-10.1.26.tar.gz .
RUN tar -xvzf apache-tomcat-10.1.26.tar.gz
RUN mv apache-tomcat-10.1.26/* .
RUN rm -rf apache-tomcat-10.1.26 apache-tomcat-10.1.26.tar.gz
ADD https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/sample.war webapps
EXPOSE 8080
CMD [ "/opt/tomcat/bin/catalina.sh","run"]
