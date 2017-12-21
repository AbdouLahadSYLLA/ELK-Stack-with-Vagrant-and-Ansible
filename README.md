# Building an ELK Stack with Vagrant and Ansible

This is the source code to along with the blog article [ELK-Stack-with-Vagrant-and-Ansible](http://xplordat.com/2017/12/12/elk-stack-with-vagrant-and-ansible/)

* Make sure that the host has sufficient CPU & RAM to build 7 vms as this one does.
* You can adjust the memory requirements in 'inventory.yml'.

Briefly:

```
vagrant up --no-provision
ansible-playbook -v -i inventory.yml elk.yml

```
For testing,

1. Generate logs on a filebeat host, say filebeat-1

```
vagrant ssh filebeat-1
cd /vagrant
./files/genLogs.pl
````

2. Open a browswer to Kibana and explore.

```
http://192.168.33.28:5601

```



	



