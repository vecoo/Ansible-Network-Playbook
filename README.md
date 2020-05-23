# My Ansible Projects
Cisco switches and router scripts in Python & YAML

Using Ansible 2.1.

This repository contains working simple examples of my projects to display my knowledge and experience with network automation. I am presenting some scripts I have used for example executing a show clock output from Cisco IOS switches using YAML. Following installation procedure was verified working on Kali Linux. Ansible playbook was executed on Cisco C2960X, IOS 15.2(2)E1 switches.


# Install Ansible

Ensure you are using Ansible v2.1 or above:

    ansible-playbook --version

If not install the latest version via your OS packager, for more information see http://docs.ansible.com/ansible/intro_installation.html

# Clone this repository to your working folder

Copy of all files in this repository will be downloaded to your mac/pc/whatever.

    $ git clone git@github.com:brona/ansible-cisco-ios-example.git

# [Optional] Edit your hosts file

If you will be using IP addresses directly in you inventory file or if you have properly working internal DNS you can skip this step.

    $ sudo nano /etc/hosts

Example hosts file on Mac OS X:

    127.0.0.1 localhost
    255.255.255.255 broadcasthost
    ::1             localhost

    10.0.0.1 switch1
    10.0.0.2 switch2

# Edit inventory

Add all network devices you want to gather time from to inventory file.

    $ cd ansible-cisco-ios-example
    $ nano inventory

# Example inventory file:

    [ios_devices]
    switch1
    switch2

# Run show_clock Playbook

    $ ansible-playbook show_clock.yml
    Username: ...
    Password: ...
    ...

Playbook will prompt you for username and password that will be used to log in to inventory devices. Gathered output will be printed on screen.
