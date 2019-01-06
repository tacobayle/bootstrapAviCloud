# bootstrapAviCloud
Prerequisites:
- Make sure Ansible is installed
- Make sure the Avi SDK is installed with appropriate version( pip list | grep avi ):
	- pip install avisdk --upgrade
        - ansible-galaxy install -f avinetworks.avisdk
- Make sure Avi Controller is reachable
- Make sure the cloud is ready/reachable to be added in the avi config.

Use the ansible playbook to
- Bootstrap the Avi controller with a new password with the parameters in vars/creds.yml
- modify the tenant settings with the parameters in vars/params.yml
- modify the default cloud as an OpenStack cloud with the parameters in vars/params.yml
# need to add other cloud capabilities in the future (LSC...)

Example:
ansible-playbook bootstrapAviCloud.yml

Script has been tested against:
- Avi 17.2.14
- Ansible 2.7.0
