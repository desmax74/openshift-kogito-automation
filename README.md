# Openshift Kogito automation

Ansible scripts to automate creation of CRC cluster and the deploy of one of the Kogito examples with just one command line.

CRC 1.7.0, and Ansible must be installed.
No previous CRC setup (no /home/{user}/.crc folder), otherwise the create script will fail, delete .crc if you want run more than once the create playbook

### Create an account on cloud.redhat.com
https://cloud.redhat.com/openshift/install and download or copy your Pull secret from the the laptop installation https://cloud.redhat.com/openshift/install/crc/installer-provisioned

The create playbook will create from scratch the crc setup, the project namespace, then download  and install Kogito Operator and Kogito CLI.
The name of the Project to create and the Pull secret will be asked in the beginning of the run.
To use the default project name (my-kogito-project) just press enter.
```sh
ansible-playbook ./playbook_create.yaml
```
Note: The CRC start spent 10 minute on a laptop, cut to few seconds in the video recording

Video Duration: 1:39 min.
[![asciicast](https://asciinema.org/a/313700.png)](https://asciinema.org/a/313700)


To deploy one of the kogito examples, enter the name of one of the example,
at the end the browser show you the login page, the output of the deploy with the instructions to see
the logs from cli will be on the ansible output.
```sh
ansible-playbook ./playbook_deploy.yaml
```
Video Duration 27:sec
[![asciicast](https://asciinema.org/a/313703.png)](https://asciinema.org/a/313703)
