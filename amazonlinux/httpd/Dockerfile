
FROM amazonlinux
RUN cd /
RUN yum install httpd -y
RUN chmod 777 .
COPY index.html /var/www/html/
EXPOSE 80
CMD httpd -D FOREGROUND
