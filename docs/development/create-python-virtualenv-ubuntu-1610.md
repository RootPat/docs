---
author:
  name: Christopher Piccini
  email: cpiccini11@gmail.com
description: 'A Python Virtual environment is a tool to create an isolated environment within your VPS.'
keywords: 'python,python virtual environment,keywords,virtualenv,pip'
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
modified: Wednesday, August 14, 2017
modified_by:
  name: Linode
published: 'Wednesday, August 13, 2017'
title: 'Create a Python Virtual Environment in Ubuntu 16.10'
contributor:
  name: Christopher Piccini
  link: https://twitter.com/chrispiccini11
external_resources:
- '[virtualenv Documentation](http://virtualenv.pypa.io/)'
---


## Introduction
The purpose of this guide is to allow you to create and run Python virtual environments in your Ubuntu 16.10 linode.  A Python Virtual environment or `virtualenv` is a tool to create an isolated Python environment within your VPS.  This can be extremely powerful as you can create a virtual environment and install all Python executables/packages to it, and it will have no dependencies outside of your created virtual environment.



## Before You Begin

1.  This guide will use `sudo` wherever possible. Complete the sections of our [Securing Your Server](https://www.linode.com/docs/security/securing-your-server) to create a standard user account, harden SSH access and remove unnecessary network services. Do **not** follow the Configure a Firewall section yet--this guide includes firewall rules specifically for an OpenVPN server.

2.  Update your system:

        sudo apt get update
 

    {: .note}
    >
    > This guide is written for a non-root user. Commands that require elevated privileges are prefixed with `sudo`. If you’re not familiar with the `sudo` command, see the [Users and Groups](https://www.linode.com/docs/tools-reference/linux-users-and-groups) guide. Replace each instance of `testuser` in this guide with your custom user account.

## Installing Virtual Environment
1.  Run this command to install Python's virtual environment.
        
        sudo apt install virtualenv
 

## Create New Directory in Home
1.  Navigate to your users home directory.

        cd 

2.  Create directory named *python-environments*

        mkdir python-environments

3.  Navigate in the newly created directory.

        cd python-environments

## Create a Virtual Environment in Python3
1.  Enter command to create a virtual environment in Python 3 with the environment name of *env*
        
        virtualenv -p python3 env

2.  Validate that environment is installed with python3.
        
        ls env/lib

## Activate Environment
1.  Enter command to activate the newly created virtual environment. The name of the working environment will appear in parentheses.
        
        source env/bin/activate
        (env) testuser@localhost:~/python-environments$

    Now that the environment is active, you can install executables and packages only to this virtual environment.

## Deactivate Environment.
1.  Enter command in an active virtual environment to deactivate virtual environment.
        
        deactivate






