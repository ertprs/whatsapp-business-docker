FROM docker.whatsapp.biz/web:v2.25.3

COPY lighttpd /etc/init.d/lighttpd
COPY web_setup.sh /opt/whatsapp/bin/web_setup.sh
COPY launch_within_docker.sh /opt/whatsapp/bin/launch_within_docker.sh
RUN  chmod 775 /opt/whatsapp/bin/launch_within_docker.sh

RUN  mkdir -p /usr/local/waent /var/lib/whatsapp /var/log/lighttpd /var/run/lighttpd
RUN  touch /etc/wa_config.json
RUN  chmod -Rf 775 /etc/wa_config.json /etc/lighttpd /etc/php /etc/init.d/lighttpd 
RUN  chmod -Rf 775 /var/www /var/log /var/run /var/lib/whatsapp 
RUN  chmod -Rf 775 /usr/local/waent 

RUN  chown -Rf root:root /var/log/lighttpd /var/www
