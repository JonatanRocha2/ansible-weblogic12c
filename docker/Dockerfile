FROM centos:7

RUN yum -y update
RUN yum -y install httpd
RUN yum -y install openssh-server

CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
