# Prerequisites

## OpenStack Cloud Platform

This tutorial leverages the [Xena OpenStack cloud platform](https://docs.openstack.org/xena/?_ga=2.146439153.47571380.1641563000-92394932.1641563000) to streamline provisioning of the compute infrastructure required to bootstrap a Kubernetes cluster from the ground up. It assumes you have an OpenStack cluster available to use!

## OpenStack Cloud Platform Client

### Install the OpenStack Client

Follow the Client [documentation](https://docs.openstack.org/python-openstackclient/xena/) to install and configure the `openstack` command line utility.

Verify the OpenStack client version is 5.3.1 or higher:

```
openstack --version
```

### Set a Default Project

This tutorial assumes a default Project have been configured.

If you are using the `openstack` command-line tool for the first time, download the OpenStack RC file from your Horizon instance (under your usrename on the right hand side drop down menu) and source it.

```
$ source training-openrc.sh
Please enter your OpenStack Password for project training as user john:
```

## Running Commands in Parallel with tmux

[tmux](https://github.com/tmux/tmux/wiki) can be used to run commands on multiple compute instances at the same time. Labs in this tutorial may require running the same commands across multiple compute instances, in those cases consider using tmux and splitting a window into multiple panes with synchronize-panes enabled to speed up the provisioning process.

> The use of tmux is optional and not required to complete this tutorial.

![tmux screenshot](images/tmux-screenshot.png)

> Enable synchronize-panes by pressing `ctrl+b` followed by `shift+:`. Next type `set synchronize-panes on` at the prompt. To disable synchronization: `set synchronize-panes off`.

Next: [Installing the Client Tools](02-client-tools.md)
