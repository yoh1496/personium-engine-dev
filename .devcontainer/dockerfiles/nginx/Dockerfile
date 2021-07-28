FROM nginx:1.14

RUN apt-get update && apt-get install -y \
  vim \
  curl \
  jq

COPY etc/nginx.conf /etc/nginx/nginx.conf

COPY etc/conf.d/default.conf /etc/nginx/conf.d/default.conf
COPY entrypoint.sh /

RUN chmod +x /entrypoint.sh

EXPOSE 443
EXPOSE 80

ENTRYPOINT [ "/entrypoint.sh" ]
