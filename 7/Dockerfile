FROM registry.access.redhat.com/rhel7

LABEL maintainer "Bitnami <containers@bitnami.com>"
ENV IMAGE_OS=ol-7
ENV BITNAMI_IMAGE_VERSION=7-r33

COPY rootfs /

# component installation requirements
RUN mkdir --parents /opt/bitnami
RUN chmod 0755 / /usr /usr/local /usr/local/bin /opt && \
    yum-config-manager --enable ol7_developer_EPEL ol7_optional_latest && \
    yum upgrade -y && \
    install_packages tar gzip curl ca-certificates sudo procps-ng libaio-devel
