FROM openshift/jenkins-slave-base-centos7 

MAINTAINER Ankush Chadha <ankushc@jfrog.com>

USER root
# Install pip
RUN yum -y install epel-release && \
    yum -y install python-pip && \
    yum clean all

ENV BASH_ENV=/usr/local/bin/scl_enable \
    ENV=/usr/local/bin/scl_enable \
    PROMPT_COMMAND=". /usr/local/bin/scl_enable"

# When bash is started non-interactively, to run a shell script, for example it
# looks for this variable and source the content of this file. This will enable
# the SCL for all scripts without need to do 'scl enable'.
ADD contrib/bin/scl_enable /usr/local/bin/scl_enable
ADD contrib/bin/configure-slave /usr/local/bin/configure-slave

USER 1001 
