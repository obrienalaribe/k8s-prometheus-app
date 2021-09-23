FROM adoptopenjdk/openjdk11:ubi

RUN groupadd -r appuser &&\
    useradd -r -g appuser appuser &&\
    mkdir -p /opt/app

ARG VAULT_TOKEN
USER appuser
WORKDIR /home/appuser
RUN mkdir -p rrm/logs/rrm-configuration-service
ENV VAULT_TOKEN=${VAULT_TOKEN:-"test"}

ENTRYPOINT ["tail","-f","/dev/null"]