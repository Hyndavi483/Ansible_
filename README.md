# Ansible

# What is Ansible ?
Ansible is an open source IT automation engine.
Configuration management, Provisioning(Creation of instance, S3 bucket), Deployment(Deploying Artifact into Target Servers) and Network Automation(Automation of VLAN).
It is free to use, and the project benefits from the experience and intelligence of its thousands of contributors.

# Why Ansible?
Over 10 yrs back we had system engineers where they will maintain the configuration updates and OS updates everything they are doing manually for some servers. Since the servers are of different type.

# How Ansible works ?
Ansible is agentless in nature, which means you don't need install any software on the manage nodes.

For automating Linux and Windows, Ansible connects to managed nodes and pushes out small programs—called Ansible modules—to them. These programs are written to be resource models of the desired state of the system. Ansible then executes these modules (over SSH by default), and removes them when finished. These modules are designed to be idempotent when possible, so that they only make changes to a system when necessary.

For automating network devices and other IT appliances where modules cannot be executed, Ansible runs on the control node. Since Ansible is agentless, it can still communicate with devices without requiring an application or service to be installed on the managed node.

# Chef Vs Puppet Vs Ansible
Chef vs Puppet vs Ansible:
Puppet, Chef have a complex Learning curve. It uses Master-slave Architecture
Ansible is easy to learn. Since it uses YAML language. Uses Agentless Architecture(Control Node, Manage Node).
Control Node: Machine use for Ansible installation.
Manage Node: All the machines which are using the configuration.

# Ansible Vs Shell Vs Python:
For example we have multiple VM’s with multiple OS then if we want to install something a shell will fail for Some OS like Windows.
Python → It is Platform independent. So it will work for all VM’s. But one is we need to have a python programming language. And we need to update the script yearly. And we have 100 VM's. We need to login to 100 VM’s and execute the Code. To run all at a time paramico/fibre.
Ansible → In Control node install Ansible. In Inventory add the IP addresses. YAML Language. Easy to learn. Doesn’t require a strong programming language.

# When Python over Ansible?
We want to create tasks by using API. We will prefer Python. Ansible does not have rich API modules.

# We have Provisioning right, why Terraform rather than Ansible?
We will prefer terraform since it is a dedicated tool for Infrastructure as a code.

# Ansible installation
python3 -m pip install --user pipx
python3 -m pipx ensurepath
source ~/.zshrc  
pipx install ansible-core==2.12.3
