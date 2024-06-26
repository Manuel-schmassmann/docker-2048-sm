FROM ubuntu:22.04  

RUN apt-get update 

# install the Nginx web server, the zip utility, and the curl command-line tool in the Docker image during the image build process.
RUN apt-get install -y nginx zip curl 

# modify the Nginx configuration file within the Docker image to set the "daemon off;" option
# , ensuring that Nginx runs in the foreground when the container is launched.
RUN echo "daemon off;" >>/etc/nginx/nginx.conf 

RUN curl -o /var/www/html/master.zip -L https://codeload.github.com/gabrielecirulli/2048/zip/master

RUN cd /var/www/html/ && unzip master.zip && mv 2048-master/* . && rm -rf 2048-master master.zip

# specifies the port to be exposed for the Docker container
EXPOSE 80

# when a container is created from the image and started, it will automatically execute the Nginx binary (/usr/sbin/nginx) 
# with the specified configuration file (/etc/nginx/nginx.conf). This will start the Nginx web server within the container, using the provided configuration file.
CMD ["/usr/sbin/nginx", "-c", "/etc/nginx/nginx.conf"]