DOCKER_NAMESPACE =	armbuild/
NAME =			scw-app-jenkins-worker
VERSION =		latest
VERSION_ALIASES =	
TITLE =			Jenkins Worker
DESCRIPTION =		Jenkins Worker
SOURCE_URL =		https://github.com/scaleway/image-app-jenkins
IMAGE_VOLUME_SIZE =	50G

## Image tools  (https://github.com/scaleway/image-tools)
all:	../docker-rules.mk
../docker-rules.mk:
	$(MAKE) -C .. docker-rules.mk
-include ../docker-rules.mk
