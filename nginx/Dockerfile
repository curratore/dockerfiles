FROM centos:latest

MAINTAINER frodriguezd@gmail.com

ADD http://nginx.org/keys/nginx_signing.key /etc/yum/
RUN rpm --import /etc/yum/nginx_signing.key 

RUN rpm -Uvh http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm
RUN yum update -y && yum install nginx -y

RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log

VOLUME ["/var/cache/nginx"]

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
