# nginx/Dockerfile
FROM nginx

RUN apt-get update && \
    apt-get install -y nginx apache2-utils libapache2-mod-auth-gssapi krb5-user

COPY nginx.conf /etc/nginx/nginx.conf
COPY default.conf /etc/nginx/conf.d/default.conf
COPY HTTP.keytab /etc/nginx/HTTP.keytab

CMD ["nginx", "-g", "daemon off;"]