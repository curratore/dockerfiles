FROM centos:latest

MAINTAINER frodriguezd@gmail.com


COPY etc/yum.repos.d/nginx.repo /etc/yum.repos.d/nginx.repo
RUN yum install wget -y && \
	wget http://nginx.org/keys/nginx_signing.key && \
	rpm --import nginx_signing.key

RUN yum update -y && yum install nginx -y

RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log

VOLUME ["/var/cache/nginx"]

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]