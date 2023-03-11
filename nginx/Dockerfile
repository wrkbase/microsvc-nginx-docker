FROM nginx:latest

RUN apt-get update -y && apt-get install -y openjdk-11-jdk
RUN mkdir -p /etc/ssl/private /etc/ssl/certs
RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/site.dec.key \
    -out /etc/ssl/certs/site.crt \
    -subj "/C=US/ST=Example/L=Example/O=Example Company Inc./CN=www.example.com" \
    -passin pass:mypassword
COPY default.conf /etc/nginx/conf.d/default.conf
