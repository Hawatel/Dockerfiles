# Written by D.Iwaniuk (d.iwaniuk@hawatel.com)

FROM centos:centos7
MAINTAINER Hawatel Team <support@hawatel.com>

RUN yum -y update; yum clean all
RUN yum -y install epel-release; yum clean all
RUN yum -y install httpd; yum clean all
RUN yum -y install apachetop atop goaccess; yum clean all;
RUN echo "Hello World" >> /var/www/html/index.html

COPY ./httpd /etc/httpd
ADD httpd24.sh /httpd24.sh
RUN chmod -v +x /httpd24.sh

EXPOSE 80

CMD ["/httpd24.sh"]
