#FROM centos:7
FROM centos/systemd
ENV container docker


# Install the ScaleIO MDM dependencies
RUN yum install -y libaio numactl net-tools sysvinit-tools

# Apparently ScaleIO still uses the old ways... (firewall script require /sbin/service)
#RUN yum -y install initscripts && yum clean all
#RUN yum -y install initscripts 

# Add the necessary RPMs from the local file system
# NB - You'll need to download these RPMs from EMC and add them to the RPMS folder before building your images
#ADD RPMS/EMC-ScaleIO-mdm-2.0-13000.211.el7.x86_64.rpm /EMC-ScaleIO-mdm-2.0-13000.211.el7.x86_64.rpm
ADD RPMS/EMC-ScaleIO-mdm-*.x86_64.rpm /

# Install the ScaleIO packages
RUN rpm -Uvh EMC-ScaleIO-mdm-*.x86_64.rpm

