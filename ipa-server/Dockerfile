# ipa server on Atomic Host
# Version 1
# Clone from the rhel7 image

FROM ipa-base:latest

USER root

MAINTAINER Tony Li


ADD dbus.service /etc/systemd/system/dbus.service
ADD httpd.service /etc/systemd/system/httpd.service

ADD systemctl /usr/bin/systemctl
ADD systemctl-socket-daemon /usr/bin/systemctl-socket-daemon

ADD ipa-server-configure-first /usr/sbin/ipa-server-configure-first

RUN ln -sf dbus.service /etc/systemd/system/messagebus.service 

RUN chmod -v +x /usr/bin/systemctl /usr/bin/systemctl-socket-daemon /usr/sbin/ipa-server-configure-first 
RUN groupadd -g 389 dirsrv ; useradd -u 389 -g 389 -c 'DS System User' -d '/var/lib/dirsrv' --no-create-home -s '/sbin/nologin' dirsrv 
RUN groupadd -g 17 pkiuser ; useradd -u 17 -g 17 -c 'CA System User' -d '/var/lib' --no-create-home -s '/sbin/nologin' pkiuser

ADD volume-data-list /etc/volume-data-list
ADD volume-data-mv-list /etc/volume-data-mv-list
RUN cd / ; mkdir /data-template ; cat /etc/volume-data-list | while read i ; do if [ -e $i ] ; then tar cf - .$i | ( cd /data-template && tar xf - ) ; fi ; mkdir -p $( dirname $i ) ; rm -rf $i ; ln -sf /data${i%/} ${i%/} ; done ; \
mv /data-template/etc/dirsrv/schema /usr/share/dirsrv/schema && ln -s /usr/share/dirsrv/schema /data-template/etc/dirsrv/schema ; echo 0.5 > /etc/volume-version ; uuidgen > /data-template/build-id

EXPOSE 53/udp 53 80 443 389 636 88 464 88/udp 464/udp 123/udp 7389 9443 9444 9445 8005

VOLUME /data

CMD ["-D", "FOREGROUND"]

ENTRYPOINT /usr/sbin/ipa-server-configure-first

