## -*- docker-image-name: "armbuild/scw-app-jenkins:latest" -*-
FROM armbuild/scw-app-java:latest
MAINTAINER Scaleway <opensource@scaleway.com> (@scaleway)

# Prepare rootfs for image-builder
RUN /usr/local/sbin/builder-enter

# Upgrade packages
RUN apt-get -q update \
  && apt-get --force-yes -y -qq upgrade

RUN wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key |  apt-key add - \
  && echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list \
  && apt-get -q update \
  && apt-get install jenkins git subversion mercurial -y -qq

RUN sed -i "s/JAVA=.*/JAVA=\/opt\/java\/jdk1.8.0_33\/bin\/java/" /etc/default/jenkins

# Clean rootfs from image-builder
RUN /usr/local/sbin/builder-leave
