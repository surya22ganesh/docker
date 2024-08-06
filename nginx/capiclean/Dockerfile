FROM ubuntu
FROM nginx
WORKDIR /usr/share/nginx/html
ADD capiclean.zip .
RUN apt-get update -y && apt-get install unzip -y
RUN unzip capiclean.zip
RUN mv html/* .
RUN rm -rf 50x.html capiclean.zip html
EXPOSE 80