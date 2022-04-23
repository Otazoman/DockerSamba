FROM ubuntu:latest
MAINTAINER Fmstrat <fmstrat@NOSPAM.NO>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get upgrade -y

# Install all apps
# The third line is for multi-site config (ping is for testing later)
RUN apt-get install -y pkg-config
RUN apt-get install -y attr acl samba smbclient ldap-utils winbind libnss-winbind libpam-winbind krb5-user krb5-kdc supervisor tzdata vim
RUN apt-get install -y openvpn inetutils-ping

# Set up script and run
ADD init.sh /init.sh
RUN chmod 755 /init.sh
CMD /init.sh setup

EXPOSE 42
EXPOSE 53
EXPOSE 53/udp
EXPOSE 88
EXPOSE 88/udp
EXPOSE 123
EXPOSE 135
EXPOSE 137-138/udp
EXPOSE 139
EXPOSE 389
EXPOSE 389/udp
EXPOSE 445
EXPOSE 464
EXPOSE 464/udp
EXPOSE 636
EXPOSE 1024-1044
EXPOSE 3268-3269
EXPOSE 5722:5722
EXPOSE 49152-65535
