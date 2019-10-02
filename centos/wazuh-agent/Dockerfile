FROM centos:latest

RUN dnf install which -y

RUN rpm --import http://packages.wazuh.com/key/GPG-KEY-WAZUH
COPY wazuh-repository.txt /etc/yum.repos.d/wazuh.repo

RUN dnf install wazuh-agent -y

COPY entrypoint.sh /scripts/entrypoint.sh
