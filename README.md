# microshift-setup
Tooling and Automation to assist in the provisioning of the microshift project

## Getting Started
**System Requirements**
To run MicroShift, you need a machine with at least:

- a supported 64-bit2 CPU architecture (amd64/x86_64, arm64, or riscv64)
- 2 CPU cores
- 2GB of RAM
- 1GB of free storage space for MicroShift
- Microshift can can be deployed on on RHEL 8, CentOS Stream 8, or Fedora 34+.

## Usage
- Ansible 2.9 required
- Add RHEL8 VM's to Ansible hosts file
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

## Links: 
- [User Documentation](https://microshift.io/docs/user-documentation/)
- [Troubleshooting](https://microshift.io/docs/user-documentation/troubleshooting/)
- [MicroShift with Advanced Cluster Management](https://microshift.io/docs/user-documentation/how-tos/acm-with-microshift/)
- [Deploy a basic application](https://microshift.io/docs/user-documentation/how-tos/example-usage/)