ARG DOCKER_VERSION=latest

# create an "alias" because COPY --from does not support expanding variables.
FROM docker:${DOCKER_VERSION} AS docker

FROM jenkins/jenkins:lts-jdk11

USER root

COPY --from=docker /usr/local/bin/docker /usr/local/bin/

RUN groupadd -g 1001 docker \
    && usermod -aG docker jenkins

USER jenkins
