JAV
===

### Jekyll-Ansible-Vagrant *Starter Pack*

#### Description
This is a starter pack for quickly developing a new Jekyll project locally with Vagrant, which is then easily deployed with Github Pages. It is based on a stock Ubuntu 14.04 base image, and uses Ansible to install and configure the basic services you'll need:
 - Ruby & RubyGems & Bundler (from official RVM Ansible role)
 - Node.js (Why?)
 - Github-Pages gem (this includes Jekyll)

#### Features
- fully self-contained, installs Ansible within the VM
- develop with local Jekyll server, then deploy to Github Pages

----

#### Quick start, developing locally

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

0. Log into the VM via SSH:
    ```sh
    vagrant ssh
    ```

0. Start local Jekyll server:
    ```sh
    cd jav
    jekyll serve
    ```

0. Visit your app:
    ```
    http://jav.local
    ```

0. **Profit** :heavy_check_mark:

