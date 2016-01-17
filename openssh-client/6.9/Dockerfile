FROM buildpack-deps:vivid
MAINTAINER Jacob Marshall <jacob@manage.net.nz>

ENV OPENSSH_VERSION 6.9p1
ENV OPENSSH_MIRROR http://mirror.internode.on.net/pub/OpenBSD/OpenSSH/portable

RUN curl -SLO "${OPENSSH_MIRROR}/openssh-${OPENSSH_VERSION}.tar.gz" \
 && tar -xzf "openssh-${OPENSSH_VERSION}.tar.gz" \
 && cd "openssh-${OPENSSH_VERSION}" \
 && ./configure \
 && make \
 && make install \
 && cd .. \
 && rm "openssh-${OPENSSH_VERSION}.tar.gz" \
 && rm -rf "openssh-${OPENSSH_VERSION}"

ENTRYPOINT ["ssh"]