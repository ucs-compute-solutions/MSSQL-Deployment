# README.md


This repository contains Ansible playbook for deploying  Microsoft SQL Server pods on Red Hat Openshift Container Platform using Portworx Storage provider.

Pre-requisites: 
===========================================================================================================================

The following prerequisites needs to be completed before using this ansible script

1) This play book must be executed from a work station from which you must  be able to access the OCP cluster.
2) Ansible v2.9 or higher  must be installed on the  work station 
3) Kubernetes.core module must be installed as this ansible script uses Kubernetes.core.K8s module.
4) A valida storage class object must be already created. For instance, Portworx storage provider can be used for privisioning required volumes for SQL pod.

Steps to execute
===========================================================================================================================

1) Clone the repository to your local work station by running " git clone  https://github.com/ucs-compute-solutions/MSSQL-Deployment.git"
2) Go to MSSQL-Deployment/ folder
3) Provide your Microsoft SQL Server pod requirement deatils in the file group_vars/all.yml. This deployment
4) Deploy MSSQL Server pod by runing "ansible-playbook deploy-mssqlpod.yml"
5) To clean up the pod, run "ansible-playbook cleanup.yml".

