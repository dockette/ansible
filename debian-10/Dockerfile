FROM dockette/debian:buster-slim

RUN apt update && \
    apt dist-upgrade -y && \
    apt install -y gnupg2 python3 python3-pip curl wget && \
    echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" >> /etc/apt/sources.list.d/ansible.list && \
    apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367 && \
    apt update && \
    apt install -y ansible && \
    pip3 install "ansible-lint[community,yamllint]" && \
    rm -rf /var/cache/apk/*

CMD ["/bin/bash"]
