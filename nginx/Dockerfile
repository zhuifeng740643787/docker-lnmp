FROM nginx:1.10.3
RUN mkdir /code \
    && mkdir /access_log \
    && rm -f /etc/nginx/conf.d/default.conf \
    && rm -f /etc/nginx/nginx.conf
WORKDIR /code
COPY ./conf/conf.d/* /etc/nginx/conf.d/
COPY ./conf/nginx.conf /etc/nginx/
VOLUME ["/code/", "/access_log/"]
EXPOSE 8001 8002 8003