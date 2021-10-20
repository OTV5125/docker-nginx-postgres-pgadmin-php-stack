FROM nginx:1.21.3

RUN useradd -ms /bin/bash otv5125
COPY conf/app.conf /etc/nginx/conf.d/default.conf
COPY conf/nginx.conf /etc/nginx/nginx.conf

RUN touch /var/run/nginx.pid \
 && chown -Rf otv5125:otv5125 \
    /var/run/nginx.pid \
    /var/cache/nginx \
    /var/log/nginx \
    /etc/nginx

USER otv5125