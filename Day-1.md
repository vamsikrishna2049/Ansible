### What is Ansible?
- Ansible is a automation platform for Provisioning, Configuration management, Deployment & Network automation.

## Why Ansible?
- Ansible uses YAML and it is agent-less(No additional Software required to communicate to other nodes).
- Other tools like Puppet & Chef has more learning curve as they use Ruby & also we have to install agents on target machines.

### More details on Ansible
- Ansible was mainly built for Configuration management but extended to other automation features like Provisioning resources, Deployment & Network Automation.
- Ansible uses YAML which internally converts to Python and execute on target machines.
- Ansible has Control nodes and Managed nodes.
- Requirement is to have Python installed on both nodes & PIP for ansible installtion.

### Why ansible scripts over Bash & Python scripts?
- Less learning curve, scripts are not machine depended as Bash, less maintainence
- It is not strict advice but we can always use mix of tools as required

### Installation
- Ansible can be installed on different machines and used as Control node
- PIP should be installed 
- `pip3 install ansible` - to install ansible
- `ansible --version` - to verify ansible version

### Plugin's
- VS Code editor
- YAML & Ansible plugin's from RedHat
