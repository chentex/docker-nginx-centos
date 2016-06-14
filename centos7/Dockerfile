FROM centos:centos7
MAINTAINER Vicente Zepeda <chente.z.m@gmail.com>

ENV nginxversion="1.10.0-1" \
    os="centos" \
    osversion="7"

RUN yum install -y wget openssl sed &&\
    package-cleanup -q --leaves | xargs -l1 yum -y remove &&\
    yum clean all &&\
    wget http://nginx.org/packages/$os/$osversion/x86_64/RPMS/nginx-$nginxversion.el$osversion.ngx.x86_64.rpm &&\
    rpm -iv nginx-$nginxversion.el$osversion.ngx.x86_64.rpm &&\
    sed -i '1i\
    daemon off;\
    ' /etc/nginx/nginx.conf

CMD ["nginx"]