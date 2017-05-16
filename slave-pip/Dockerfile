FROM openshift/jenkins-slave-base-centos7 

MAINTAINER Ankush Chadha <ankushc@jfrog.com>

USER root
# Install pip
RUN yum -y install epel-release && \
    yum -y install python-pip && \
    yum clean all

USER 1001 
