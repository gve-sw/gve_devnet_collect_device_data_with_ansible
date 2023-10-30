# gve_devnet_ansible_collect_device_data

Prototype ansible playbook that pushes the command to collect the IOS device data


## Contacts

* Hyeyoung Kim (hyeyokim@cisco.com)
* Lakshya Tyagi (ltyagi@cisco.com)


## Solution Components

* Ansible
* Cisco IOS devices


## Related Sandbox Environment

[IOS XE on CSR Latest Code with ZTP functionality](https://devnetsandbox.cisco.com/RM/Diagram/Index/f2e2c0ad-844f-4a73-8085-00b5b28347a1?diagramType=Topology)


## Installation

**Clone repo:**

```bash
git clone https://github.com/gve-sw/gve_devnet_collect_device_data_with_ansible
```

**Install required dependancies:**

```bash
pip3 install -r requirements.txt
```
or 
```bash
pip install -r requirements.txt
```


## Configuration

**Configure required variables:**

Fill out all the values of the variables inside the hosts file. Below is a sample, make sure to change accordingly.

```bash
[iosxe:vars]
ansible_connection=ansible.netcommon.network_cli
ansible_user=
ansible_password=
ansible_become=yes
ansible_become_method=enable
ansible_network_os=cisco.ios.ios
subnet_id=

[iosxe]
# Write device host ip here
```


## Usage

```bash
ansible-playbook -i hosts <playbook_name>.yaml
```
**To Save log,**
```bash
ANSIBLE_LOG_PATH=<textfile_path>.txt ansible-playbook <playbook_name>.yaml
```

## Screenshots
Output of iosxe_show_interface_brief.yaml
<img src="https://wwwin-github.cisco.com/gve/gve_devnet_collect_device_data_with_ansible/blob/master/Screenshot%202023-05-15%20at%205.25.08%20PM.png" alt="Alt text" title="Optional title">



### LICENSE

Provided under Cisco Sample Code License, for details see [LICENSE](LICENSE.md)

### CODE_OF_CONDUCT

Our code of conduct is available [here](CODE_OF_CONDUCT.md)

### CONTRIBUTING

See our contributing guidelines [here](CONTRIBUTING.md)

#### DISCLAIMER

<b>Please note:</b> This script is meant for demo purposes only. All tools/ scripts in this repo are released for use "AS IS" without any warranties of any kind, including, but not limited to their installation, use, or performance. Any use of these scripts and tools is at your own risk. There is no guarantee that they have been through thorough testing in a comparable environment and we are not responsible for any damage or data loss incurred with their use.
You are responsible for reviewing and testing any scripts you run thoroughly before use in any non-testing environment.
