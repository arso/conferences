# Configuration
## Install ovirt engine
either use the oVirt appliance or install CentOS Linux 8 minimal by following these steps:
- Install the CentOS Linux 8 image from http://centos.mirror.garr.it/centos/8.1.1911/isos/x86_64/CentOS-8.1.1911-x86_64-dvd1.iso
- dnf install https://resources.ovirt.org/pub/yum-repo/ovirt-release44.rpm
- dnf update (reboot if needed)
- dnf module enable -y javapackages-tools pki-deps postgresql:12
- dnf install ovirt-engine
- dnf module enable mod_auth_openidc:2.3 -y
- dnf install mod_auth_openidc
- engine-setup

## Install Keycloak,setup client id & secret, update /etc/* configuration

## systemctl restart {ovirt-engine,httpd}
