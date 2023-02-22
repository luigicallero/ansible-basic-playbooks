# Ansible Basic Playbooks
Learning from Oreilly course ["Ansible for the Absolute Beginner - Hands-On – DevOps"](https://learning.oreilly.com/videos/ansible-for-the/9781789132427/) by Mumshad Mannambeth

## First Create the Lab:

1) Download VirtualBox:

    https://www.virtualbox.org/wiki/Downloads

2) Download a VDI (Virtual Disk Image) for a Centhos OS:

    https://www.osboxes.org/
    
    On "VM Images" menu, select "VirtualBox Images", and then under CentOS click on "Download VirtualBox (VDI) Image"

3) Generate template VM

4) Clone 3 VMs: Ansible Controller, and 2 Ansible Targets

## Ansible Playbooks
### Executing the playbooks:
```yaml
ansible-playbook PLAYBOOK_NAME.yaml -i INVENTORY_FILE
```
Example:

* Executing ping playbook with prompt on exercise-0-pingtest folder (/home/osboxes/ansible-basic-playbooks/exercise-0-pingtest)
```yaml
ansible-playbook playbook-ping.yaml -i ./inventory.txt
```

### Interesting Notes:
* playbook file can have extension .yml or .yaml, is the same.
* Majority of Ansible modultes are idempotent: will only make a change if it is required (if same file is already there it will not copy it again).
* Idempotency: an operation is idempotent if the result of performing it once is exactly the same as the result of performing it repeteadly without any intervening actions.
* Jinja2 templating exercises come from Kodecloud mini course [Jinja2 Basics](https://kodekloud.com/courses/jinja2-templating/)