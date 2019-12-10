# 
# Dockerfile for building the apache image
#

# Start from Phusion.
FROM phusion/baseimage

RUN /usr/bin/apt-get update && /usr/bin/apt-get install software-properties-common -y
RUN /usr/bin/add-apt-repository ppa:certbot/certbot && /usr/bin/apt-get update && /usr/bin/apt-get install apache2 -y

# Start the Apache2 daemon during container startup
RUN mkdir /etc/service/apache2
COPY apache2.sh /etc/service/apache2/run
RUN chmod +x /etc/service/apache2/run

# end of file
