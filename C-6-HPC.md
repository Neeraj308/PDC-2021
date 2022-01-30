# C6ReadMe
Rohan 1812202
Neeraj 1812197
Mehak Lund 1812190
Virender Chawla 1812213

## Objective
To create workload on HPC Cluster running CentOS
We can also benchmark the virtual machine's performance running CentOS on Linux hardware.

## Requirements

- CentOS with VMware
- Creating multiple CentOS

## Terminologies
1.CentOS: CentOS, which stands for the Community Enterprise Operating System, is a distribution of the Linux operating system based on RHEL (Red Hat Enterprise Linux). It runs on the x86 PAE and x86-64 architectures, and is currently the most popular Linux distribution for web servers.

## Installation & Configuration
sudo hostnamectl set-hostname masternode
it is changing the hostname (masternode).

# scp HPCNode1 root@HPCMaster
it contian the copy of HPCNode1 server in the rootHPCMaster.

scp /var/tmp/HPCNode1 root@HPCMaster
it is copying the HPCnode1.

vi /etc/sysconfig/network
it shows the system configuration.

scp /etc/hosts node1:/etc/
it copy and create the node1 in the masternode.

ssh-keygen -t dsa
generate secure shell authentication key

ssh-keygen -t rsa
it is generate the secure shell.

ssh-keyscan -t dsa node1 node2
it create the authentication key secure node 1 and node 2 in masternode.

cat *.pub >> authorized_keys
it create the authorized key.

ssh-keyscan -t dsa masternode node1 node2 >> /etc/ssh/ssh_known hosts
These hosts keys are stored at locations '/etc/ssh/known_hosts'.

ssh-keyscan -t rsa masternode node1 node2 >> /etc/ssh/ssh_known hosts
These hosts keys are store in the locations.

scp /etc/ssh/ssh_known_hosts node1
it copy the host key are stored at the location.

ssh node1
it will signin the node1

ssh node2 
it will also signin the node2 in masternode.

sudo yum -y install chrony
it install the chronyd.

vi /etc/chrony.conf
it shows the chrony configuration.

systemctl restart chronyd
restart the chronyd.

firewall-cmd --permanent --add-service=nfs






