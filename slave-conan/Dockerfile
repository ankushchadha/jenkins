FROM openshift/jenkins-slave-base-centos7 

MAINTAINER Ankush Chadha <ankushc@jfrog.com>

ENV HOME=/home/jenkins

USER root

# Install pip
RUN yum -y install epel-release && \
    yum -y install python-pip && \
    yum clean all

# Install conan
RUN pip install conan

USER 1001 
