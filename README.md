JAV
===

### Jekyll-Ansible-Vagrant *Starter Pack*

#### Description
This is a starter pack for quickly developing a new Jekyll project locally with Vagrant, which is then easily deployed with Github Pages. It is based on a stock Ubuntu 14.04 base image, and uses Ansible to install and configure the basic services you'll need:
 - Ruby & Bundler (from official RVM Ansible role)
 - Github-Pages gem (this includes Jekyll)
 - Node.js (Why?)

#### Features
- fully self-contained, installs Ansible within the VM
- develop with local Jekyll server, then deploy to Github Pages
- update Github Pages dependencies with `vagrant provision`

----

### Quick start, developing locally

0. Install [Vagrant](https://www.vagrantup.com/) ***(Requires 1.8.2+)***

0. Clone this repo:
    ```
    git clone git@github.com:paste/jav.git
    ```

0. Modify your computer's local `/etc/hosts`:

    ```
    192.168.33.33   jav.local
    ```

0. Build your Vagrant VM:

    ```sh
    vagrant up
    ```

0. Log into the VM and start local Jekyll server:
    ```sh
    vagrant ssh
    cd /vagrant
    jekyll serve
    ```

0. Visit your app:
    ```
    http://jav.local
    ```

0. **Profit** :heavy_check_mark:

