FROM nginx:1.10.1-alpine

RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    && ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 3000

COPY ./applications/mocktest-frontend/default.conf /etc/nginx/conf.d/default.conf
COPY ./applications/mocktest-frontend/mime.types /etc/nginx/mime.types
COPY ./applications/mocktest-frontend/nginx.conf /etc/nginx/nginx.conf
COPY ./applications/mocktest-frontend/dist.conf /etc/nginx/conf.d/dist.conf

COPY ./mocktest-frontend/build/ /var/www/build/

WORKDIR /var/www/build

ENTRYPOINT ["nginx", "-g", "daemon off;"]

