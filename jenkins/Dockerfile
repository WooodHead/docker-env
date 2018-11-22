FROM jenkins/jenkins:lts
LABEL maintainer="tyr@pettingzoo.co"

USER root

ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/go/bin

# Install Minio Client
RUN curl -o /usr/bin/mc https://dl.minio.io/client/mc/release/linux-amd64/mc && \
    chmod +x /usr/bin/mc

# Install Go
RUN curl -o /tmp/go1.11.2.linux-amd64.tar.gz https://dl.google.com/go/go1.11.2.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf /tmp/go1.11.2.linux-amd64.tar.gz && \
    rm -Rf /tmp/go1.11.2.linux-amd64.tar.gz

RUN go get -u github.com/gobuffalo/packr/packr && \
    cp /root/go/bin/packr /usr/local/bin/

RUN apt-get update && apt-get install -y apt-transport-https ca-certificates curl gnupg2 software-properties-common && \
    curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add - && \
    apt-key fingerprint 0EBFCD88 && \
    add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable" && \
    apt-get update && apt-get install -y docker-ce && \
    rm -rf /var/lib/apt/lists/*

RUN echo "jenkins ALL=(ALL) NOPASSWD: /usr/bin/docker" >> /etc/sudoers

USER jenkins
