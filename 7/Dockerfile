FROM registry.access.redhat.com/rhel7

LABEL maintainer="Bitnami <containers@bitnami.com>" \
      name="RHEL Extras Base" \
      version="7.x" \
      release="4" \
      io.k8s.display-name="RHEL Extras Base 7.x" \
      vendor="Bitnami" \
      summary="Bitnami RedHat Enterprise Linux base image with extras base." \
      usage="This image is a generic image for Bitnami containers." \
      description="Bitnami RedHat Enterprise Linux base image with extras base." \
      io.k8s.description="Bitnami RedHat Enterprise Linux base image with extras base." \
      architecture="x86_64"

ENV IMAGE_OS=ol-7
ENV BITNAMI_IMAGE_VERSION=7-r97

COPY rootfs /

# component installation requirements
RUN mkdir --parents /opt/bitnami
RUN chmod 0755 / /usr /usr/local /usr/local/bin /opt && \
    yum-config-manager --enable ol7_developer_EPEL ol7_optional_latest && \
    yum upgrade -y && \
    install_packages tar gzip curl ca-certificates sudo procps-ng libaio-devel
