# ipa
ipa on RHEL atomic Host

run ipa-server on RHEL Atomic Host 

docker pull tonyli71/ipa-server

docker run –name ipa-server-container -ti -e IPA_SERVER_IP=192.168.0.250 -h ipa.tli.redhat.com -e PASSWORD=redhat123 -v /var/lib/ipa-data:/data -p 53:53/udp -p 53:53 -p 80:80 -p 443:443 -p 389:389 -p 636:636 -p 88:88 -p 464:464 -p 88:88/udp -p 464:464/udp -p 123:123/udp -p 7389:7389 -p 9443:9443 -p 9444:9444 -p 9445:9445 –cap-add SYS_TIME ipa-server

IPA_SERVER_IP shoud be your RHEL Atomic Host pubic ip address ( such as 192.168.0.250 )

### set static ip address on the ip-server container

docker run --privileged --name ipa-server -ti -e IPA_SERVER_IP=10.128.0.11 -e PASSWORD=redhat123 -v /var/lib/ipa-bj-data:/data -p 53:53/udp -p 53:53 -p 80:80 -p 443:443 -p 389:389 -p 636:636 -p 88:88 -p 464:464 -p 88:88/udp -p 464:464/udp -p 123:123/udp -p 7389:7389 -p 9443:9443 -p 9444:9444 -p 9445:9445 --dns 8.8.8.8 -e FORWARDER=127.0.0.1 -e ETH0_IP=10.128.0.252 -h ipa.gcg.redhat.com  ipa-server
