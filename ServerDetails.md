# **IITB Server Details**

## Proxy Server To access via SSH

SSH Link: tejaswmc@login.iitb.ac.in -p 5022
This uses a IITB-Tejas-Machine Keys stored in Mac Home directory

## Proxmox Server Details

Proxmox IP = 10.204.1.102
root/prox1@wmc007
OS = proxmox 7.4-3

 

## Kube VM details : ( OS = Ubuntu 22.04 LTS)

Master Node = 10.204.1.121  k8s/123456
Worker Node1 = 10.204.1.122  k8s/123456
Worker Node2 = 10.204.1.123  k8s/123456
Lagoon = 10.204.1.124  k8s/123456
Anydesk = 10.204.1.125 anyd/@nyD007 
Anydek ID: 1874189917 passwd : @nyD$007

## IITB Network

Userid => tj.guest6
Password => 5K#D#vnz
Token For Curk => 7004b93722500c13e3b70bbff84c3908

## To connect internt on any VM using terminal curl command

curl --location-trusted -u tj.guest6:7004b93722500c13e3b70bbff84c3908 "https://internet-sso.iitb.ac.in/login.php" > /dev/null

## rook Installation Guide 

https://www.talos.dev/v1.6/kubernetes-guides/configuration/ceph-with-rook/


## Ceph Cluster Dashboard
Ceph Dashboard Url : https://10.204.1.121:30198/#/dashboard
Password : -n6-|W-ONFP6SF3aga*)

## created a Ceph s3 compatible bucket

BUCKET_HOST = rook-ceph-rgw-ceph-objectstore.rook-ceph.svc
BUCKET_PORT = 80
BUCKET_NAME = ceph-lagoon-d1831f48-864b-494f-bc10-3a906dd8c2d0
AWS_ACCESS_KEY_ID = 81EDG77241DLN3X1S1MD
AWS_SECRET_ACCESS_KEY = 3aYyOWoInhHWhfzqEbQGYrdsTdbGRApULd4WirUm


Cron Tab for continued internet access
crontab <<'EOF'
SHELL=/bin/bash
#min hr md mo wkday command
*/5 *  *  *  *     curl --location-trusted -u tj.guest6:7004b93722500c13e3b70bbff84c3908 "https://internet-sso.iitb.ac.in/login.php" > /dev/null
EOF