FROM httpd:2.4

#Update the OS
RUN apt-get update

#Install net tool
RUN apt-get install net-tools -y

#Create a proxy local sites folder, a location to have proxypass #setting
RUN mkdir -p /usr/local/apache2/conf/sites

#Copy enable and load httpd conf files that it locate conf/sites
COPY conf/httpd.conf /usr/local/apache2/conf/httpd.conf

EXPOSE 80

CMD ["httpd-foreground"]
