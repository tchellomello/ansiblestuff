FROM centos:7

MAINTAINER Marcelo Moreira de Mello <tchello.mello@gmail.com>

RUN yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN yum -y install python-pip PyYAML \
    python-jinja2 python-httplib2 python-keyczar python-paramiko python-setuptools
RUN pip install ansible

# ansible
COPY main.yml /ansible/
COPY tasks /ansible/tasks/

RUN ansible-playbook -i "localhost," -c local -t docker /ansible/main.yml 

EXPOSE 80

CMD ["/sbin/nginx", "-g", "daemon off;"]
