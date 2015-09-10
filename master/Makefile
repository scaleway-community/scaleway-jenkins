DOCKER_NAMESPACE =	armbuild/
NAME =			scw-app-jenkins
VERSION =		latest
VERSION_ALIASES =
TITLE =			Jenkins Master
DESCRIPTION =		Jenkins Master
SOURCE_URL =		https://github.com/scaleway/image-app-jenkins
VENDOR_URL =		https://jenkins-ci.org/

IMAGE_VOLUME_SIZE =	50G
IMAGE_BOOTSCRIPT =	stable
IMAGE_NAME =		Jenkins Master

## Image tools  (https://github.com/scaleway/image-tools)
all:	../docker-rules.mk
../docker-rules.mk:
	$(MAKE) -C .. docker-rules.mk
-include ../docker-rules.mk
