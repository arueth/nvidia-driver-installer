ARG base_image

FROM ${base_image}

ARG rh_username
ARG rh_password

RUN subscription-manager register --username=${rh_username} --password=${rh_password} --auto-attach \
&& yum install -y gcc make kernel-devel kernel-headers
#&& subscription-manager unregister

COPY docker-entrypoint.sh /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]
