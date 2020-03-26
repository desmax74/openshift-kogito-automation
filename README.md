# Openshift Kogito automation

Ansible and scripts to automate openshift-drools-hacep-automation with just one command line.

CRC 1.7.0, and Ansible must be installed.
No previous CRC setup (no /home/{user}/.crc folder), otherwise the create script will fail.

### Create an account on cloud.redhat.com
https://cloud.redhat.com/openshift/install and download or copy your Pull secret from the the laptop installation https://cloud.redhat.com/openshift/install/crc/installer-provisioned

Create from scratch the crc setup, the project namespace, then download  and install Kogito Operator and Kogito CLI.
The name of the Project to create and the Pul secret will be asked in the beginning of the run.
```sh
ansible-playbook ./playbook_create.yaml
```
Note: The CRC start spent 10 minute, cut to few seconds in the video recording

[![asciicast](https://asciinema.org/a/313707.png)](https://asciinema.org/a/313707)

After some minutes the setup of the four Operators
Kogito, Keycloak, Infinispan, Strimzi
we could run the start script.

It deploy drools-quarkus-example build and open the CRC UI, in the  
Ansible output we will see the command to see the log of the build of the service deployed (Drools-quarkus-example).
Create from scratch the crc setup, namespace download and install operator and Kogito CLI
```sh
ansible-playbook ./playbook_deploy.yaml
```
[![asciicast](https://asciinema.org/a/313703.png)](https://asciinema.org/a/313703)


@TODO provides a Menu with all the projects available in the examples repo
