FROM nginx
LABEL MAINTAINER="manideep.thamma@nslhub.com" version=1.0
RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log
EXPOSE 3000
COPY ./applications/mocktest-frontend/default.conf /etc/nginx/sites-available/default
COPY ./applications/mocktest-frontend/mime.types /etc/nginx/mime.types
COPY ./applications/mocktest-frontend/nginx.conf /etc/nginx/nginx.conf
COPY ./applications/mocktest-frontend/dist.conf /etc/nginx/sites-available/dist
RUN ln -s /etc/nginx/sites-available/dist /etc/nginx/sites-enabled/
COPY ./build /var/www/dist/
ENTRYPOINT ["nginx", "-g", "daemon off;"]
