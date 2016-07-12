# ansible-container-jenkins

Jenkins Docker container managed with [Ansible Container](https://www.ansible.com/ansible-container).  Configures Jenkins, [jobs](ansible/jobs.yml) and [users](ansible/main.yml).

## TLDR;
First [install ansible-container](https://github.com/ansible/ansible-container/blob/master/INSTALL.md), then [*ansible-container build*](http://docs.ansible.com/ansible-container/reference/build.html), [*run*](http://docs.ansible.com/ansible-container/reference/run.html), [*push*](http://docs.ansible.com/ansible-container/reference/push.html) and [*shipit*](http://docs.ansible.com/ansible-container/reference/shipit.html).

####Ansible Container Build

```
$ cd ansible-container-jenkins
$ ansible-container build
(Re)building the Ansible Container image.
Building Docker Engine context...
Starting Docker build of Ansible Container image (please be patient)...
Ansible Container image has ID sha256:63cd919fd1d02ec6d33d01aa4441008549cc9e0a8846a52911f94bfc6ca4aec9
Starting Docker Compose engine to build your images...
Attaching to ansible_ansible-container_1
Cleaning up Ansible Container builder...
Attaching to ansible_jenkins_1, ansible_ansible-container_1
ansible-container_1  |
ansible-container_1  | PLAY [jenkins] *****************************************************************
ansible-container_1  |
ansible-container_1  | TASK [setup] *******************************************************************
ansible-container_1  | ok: [jenkins]
ansible-container_1  |
ansible-container_1  | TASK [Debug] *******************************************************************
ansible-container_1  | ok: [jenkins] => {
ansible-container_1  |     "hostvars[inventory_hostname]": {
ansible-container_1  |         "ansible_all_ipv4_addresses": [
ansible-container_1  |             "172.17.0.2"
ansible-container_1  |         ],
....
snip
...
ansible-container_1  |
ansible-container_1  | PLAY RECAP *********************************************************************
ansible-container_1  | jenkins                    : ok=5    changed=0    unreachable=0    failed=0
ansible-container_1  |
ansible_ansible-container_1 exited with code 0
Aborting on container exit...
Stopping ansible_jenkins_1 ... done
Exporting built containers as images...
Flattening image...
Exported ansible-container-jenkins-jenkins with image ID sha256:9ae4b67c72e6d10f84b922db87753726f8c2b49d9b2b537aa088386c06a69725
Cleaning up jenkins build container...
Cleaning up Ansible Container builder...
```

####Ansible Container Run

```
$ ansible-container run 
Attaching to ansible_ansible-container_1
Cleaning up Ansible Container builder...
Attaching to ansible_jenkins_1
....
snip

```