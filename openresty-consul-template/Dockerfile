FROM openresty/openresty:1.13.6.2-alpine

ENV CONSUL_TEMPLATE_VERSION 0.19.5
RUN  cd /tmp \
  && apk update \
  && apk --no-cache add \
    curl \
    zip \
  && curl -SLO https://releases.hashicorp.com/consul-template/${CONSUL_TEMPLATE_VERSION}/consul-template_${CONSUL_TEMPLATE_VERSION}_linux_amd64.zip \
  && unzip consul-template_${CONSUL_TEMPLATE_VERSION}_linux_amd64.zip  -d /usr/bin \
  && chmod +x /usr/bin/consul-template \
  && rm consul-template_${CONSUL_TEMPLATE_VERSION}_linux_amd64.zip \
  && cd ..