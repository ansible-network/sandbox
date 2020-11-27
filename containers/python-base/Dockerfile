FROM registry.access.redhat.com/ubi8/ubi

RUN dnf update -y \
  && dnf install -y python3-pip \
  && dnf clean all \
  && rm -rf /var/cache/dnf

RUN pip3 install --no-cache-dir dumb-init

ENTRYPOINT ["/usr/local/bin/dumb-init", "--"]
