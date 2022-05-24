# microshift-setup
Tooling and Automation to assist in the provisioning of the microshift project

## Usage
- Ansible 2.9 required
- Add RHEL8 VM's to ansible hosts file
- Replace CHANGEME in playbook - remote-user, RH Subscription Credentials, and PoolID to
- Run Playbook

## Replace CHANGEME in rhel8-microshift-install.yaml playbook 
- remote-user 
- RH Subscription Credentials
- PoolID

## Update inventory File

## Run Ansible playbook
```
ansible-playbook -i inventory rhel8-microshift-install.yaml
```
## Wait for restart 

## Copy Kubeconfig 
```
mkdir ~/.kube
sudo cat /var/lib/microshift/resources/kubeadmin/kubeconfig > ~/.kube/config
```

## View Pods 
```
oc get pods -A
```

