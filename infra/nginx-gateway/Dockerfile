FROM nginx:1.27

ARG SOURCE_URL
LABEL org.opencontainers.image.source=$SOURCE_URL

COPY conf.d/ /etc/nginx/conf.d/
COPY certs/ /etc/nginx/certs/
EXPOSE 443
