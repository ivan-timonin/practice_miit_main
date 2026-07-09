FROM nginx:alpine

RUN apk add --no-cache openssl

RUN mkdir -p /etc/nginx/certs && \
    openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
    -keyout /etc/nginx/certs/server.key \
    -out /etc/nginx/certs/server.crt \
    -subj "/C=RU/ST=Moscow/L=Moscow/O=Test/CN=localhost"

COPY nginx.conf /etc/nginx/nginx.conf
