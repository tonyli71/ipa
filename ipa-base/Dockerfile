# ipa server on Atomic Host
# Version 1
# Clone from the rhel7 image

#FROM rhel7:latest
FROM rhel7/rhel-tools:latest

USER root

MAINTAINER Tony Li

# Install IPA server

ADD local.repo /etc/yum.repos.d/local.repo

RUN mkdir -p /run/lock 

RUN yum --disablerepo=* --enablerepo=lrhel* install -y deltarpm yum-utils  

RUN yum --disablerepo=* --enablerepo=lrhel* install -y 389-ds-base  


RUN yum --disablerepo=* --enablerepo=lrhel* install -y bind bind-dyndb-ldap 

RUN yum --disablerepo=* --enablerepo=lrhel* install -y perl 

RUN yum --disablerepo=* --enablerepo=lrhel* install -y tomcat 

RUN yum --disablerepo=* --enablerepo=lrhel* install -y xorg-x11-utils 

RUN yum --disablerepo=* --enablerepo=lrhel* install -y certmonger

RUN yum --disablerepo=* --enablerepo=lrhel* install -y wget

RUN yum --disablerepo=* --enablerepo=lrhel* install -y java-1.7.0-openjdk

RUN yum --disablerepo=* --enablerepo=lrhel* install -y log4j

RUN yum --disablerepo=* --enablerepo=lrhel* install -y pango

RUN yum --disablerepo=* --enablerepo=lrhel* install -y tar

RUN yum --disablerepo=* --enablerepo=lrhel* install -y zip

RUN yum --disablerepo=* --enablerepo=lrhel* install -y ipa-client  

RUN yum --disablerepo=* --enablerepo=lrhel* install -y GConf2                                                   

RUN yum --disablerepo=* --enablerepo=lrhel* install -y acl                                                    

RUN yum --disablerepo=* --enablerepo=lrhel* install -y ant antlr-tool                                              

RUN yum --disablerepo=* --enablerepo=lrhel* install -y apache-commons-cli apache-commons-codec apache-commons-io apache-commons-lang                                       
RUN yum --disablerepo=* --enablerepo=lrhel* install -y apr apr-util                                                 

RUN yum --disablerepo=* --enablerepo=lrhel* install -y args4j                                                 

RUN yum --disablerepo=* --enablerepo=lrhel* install -y bcel                                                      
RUN yum --disablerepo=* --enablerepo=lrhel* install -y bea-stax bea-stax-api                                             
RUN yum --disablerepo=* --enablerepo=lrhel* install -y codemodel                                                  
RUN yum --disablerepo=* --enablerepo=lrhel* install -y dom4j                                                   
RUN yum --disablerepo=* --enablerepo=lrhel* install -y easymock2                                               
RUN yum --disablerepo=* --enablerepo=lrhel* install -y fontawesome-fonts                                     
RUN yum --disablerepo=* --enablerepo=lrhel* install -y glassfish-dtd-parser glassfish-fastinfoset glassfish-jaxb glassfish-jaxb-api                                       
RUN yum --disablerepo=* --enablerepo=lrhel* install -y hamcrest                                                   
RUN yum --disablerepo=* --enablerepo=lrhel* install -y hsqldb                                                
RUN yum --disablerepo=* --enablerepo=lrhel* install -y httpcomponents-client httpcomponents-core httpd httpd-tools
RUN yum --disablerepo=* --enablerepo=lrhel* install -y ipa-admintools                                      
RUN yum --disablerepo=* --enablerepo=lrhel* install -y isorelax                                   
#RUN yum --disablerepo=* --enablerepo=lrhel* install -y istack-commons                                            
RUN yum --disablerepo=* --enablerepo=lrhel* install -y java-1.7.0-openjdk-devel java-atk-wrapper javassist jaxen jakarta-commons-httpclient jakarta-oro
RUN yum --disablerepo=* --enablerepo=lrhel* install -y jboss-annotatbons-1.1-api jdom jettison jing jss junit jvnet-parent
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  krb5-pkinit krb5-server
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  ldapjdk                                                  
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  libunistring                                             
#RUN yum --disablerepo=* --enablerepo=lrhel* install -y  logrotate                                                
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  memcached                                               
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  mod_auth_kerb mod_nss mod_wsgi mozjs17
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  net-tools                                   
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  open-sans-fonts                                           
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  perl-Business-ISBN perl-Business-ISBN-Data perl-Crypt-SSLeay perl-Digest perl-Digest-MD5 perl-Encode-Locale
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  perl-File-Listing perl-File-Slurp                                        
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  perl-HTTP-Cookies perl-HTTP-Daemon perl-HTTP-Date perl-HTTP-Message perl-HTTP-Negotiate                                       perl-HTML-Parser perl-HTML-Tagset perl-IO-HTML perl-IO-Socket-IP perl-IO-Socket-SSL perl-LWP-MediaTypes perl-Net-HTTP perl-Net-LibIDN perl-Net-SSLeay perl-TimeDate perl-URI perl-WWW-RobotRules perl-XML-LibXML perl-XML-NamespaceSupport perl-XML-SAX perl-XML-SAX-Base perl-libwww-perl
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  pki-base pki-ca pki-server pki-tools 
#RUN yum --disablerepo=* --enablerepo=lrhel* install -y  polkit polkit-pkla-compat 
RUN yum --disablerepo=* --enablerepo=lrhel* install -y  python-memcached python-requests python-urllib3
#RUN yum --disablerepo=* --enablerepo=lrhel* install -y  qdox 
#RUN yum --disablerepo=* --enablerepo=lrhel* install -y  redhat-access-plugin-ipa redhat-logos 

RUN yum --disablerepo=* --enablerepo=lrhel* install -y ipa-server  

RUN yum --disablerepo=* --enablerepo=lrhel* install -y openssh-server  

RUN yum-config-manager --disable *-eus-* *-htb-* *-ha-* *-rt-* *-lb-* *-rs-* *-sap-* > /dev/null

RUN yum --disablerepo=* --enablerepo=lrhel*  update -y

RUN yum clean all ; rm /etc/yum.repos.d/local.repo

