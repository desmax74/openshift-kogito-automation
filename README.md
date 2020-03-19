# Openshift Kogito automation

Ansible and scripts to automate openshift-drools-hacep-automation with just one command line.

CRC 1.7.0, and Ansible must be installed.

### Create an account on cloud.redhat.com
https://cloud.redhat.com/openshift/install and download or copy your Pull secret from the the laptop installation https://cloud.redhat.com/openshift/install/crc/installer-provisioned

Create from scratch the crc setup, namespace download and install operator and Kogito CLI
```sh
ansible-playbook ./playbook_create.yaml
```
Note: The CRC setup spent 10 minute, cut to 1 minute in the video recording

[![asciicast](https://asciinema.org/a/311620.png)](https://asciinema.org/a/311620)

Deploy drools-quarkus-example build and open the CRC UI
Create from scratch the crc setup, namespace download and install operator and Kogito CLI
```sh
ansible-playbook ./playbook_start.yaml
```
