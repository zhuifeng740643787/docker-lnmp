FROM mysql:5.6
ENV MYSQL_ROOT_PASSWORD='111111' 
ENV MYSQL_USER mysql
COPY ./start.sh /
RUN chmod 755 /start.sh
ENTRYPOINT ["/start.sh"]
VOLUME ["/var/log/mysql/"]