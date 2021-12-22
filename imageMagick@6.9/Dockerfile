FROM centos:centos7

RUN yum -y install epel-release wget

RUN wget http://rpms.remirepo.net/enterprise/7/remi/x86_64/remi-release-7.9-2.el7.remi.noarch.rpm && \
    rpm -Uvh remi-release-7.9-2.el7.remi.noarch.rpm

RUN wget http://download1.rpmfusion.org/free/el/rpmfusion-free-release-7.noarch.rpm && \
rpm -Uvh rpmfusion-free-release-7.noarch.rpm

RUN yum --enablerepo=remi install -y ImageMagick6 ImageMagick6-devel ImageMagick6-heic