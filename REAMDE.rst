http://docs.openstack.org/developer/devstack/









Installation of the OpenSSH client and server applications is simple.
To install the OpenSSH client applications on your Ubuntu system, use this command at a terminal prompt::

    sudo apt-get install openssh-client

To install the OpenSSH server application, and related support files, use this command at a terminal prompt::

    sudo apt-get install openssh-server

The openssh-server package can also be selected to install during the Server Edition installation process.


::

    git clone -b stable/kilo https://github.com/openstack-dev/devstack.git

1. Download DevStack::

    git clone https://git.openstack.org/openstack-dev/devstack

The devstack repo contains a script that installs OpenStack and templates for configuration files

2. Configure

We recommend at least a Minimal Configuration be set up.

3. Add Stack User

Devstack should be run as a non-root user with sudo enabled (standard logins to cloud images such as “ubuntu” or “cloud-user” are usually fine).

You can quickly create a separate stack user to run DevStack with::

    devstack/tools/create-stack-user.sh; su stack
    sudo passwd stack

5. Start the install::

    cd devstack; ./stack.sh

It takes a few minutes, we recommend reading the script while it is building.
