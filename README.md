# Ansible for desktop

A simple and quick way to provision your development machine.

Tested with:

* Ansible 2.6
* Ubuntu 18.04 (bionic)

## Features

- Zsh, NeoVIM, Tmux
- Chrome, Firefox
- PGP, Tor, Password Manager
- NTP and localization
- Ruby, Java, Clojure
- Redis, ES, MySQL
- Vritualbox, Vagrant
- Dropbox
- Rocketchat, Skype, Slack
- i3 Window Manager
- Yunikey support
- Dotfiles
- Coding fonts
- and more...

## Installation

Checkout the [Getting Started](https://github.com/krisleech/ansible-desktop/wiki/Getting-started) guide
for an overview and examples of the recipies used.

### Ansible

Note: We use the Ansible PPA because the Ubuntu repository contains the older
2.0 version.

```
sudo add-apt-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install git vim ansible
git clone git@github.com:krisleech/ansible-desktop.git
cd ansible-desktop
```

You can also install Ansible from [source](http://docs.ansible.com/ansible/intro_installation.html).


## Configure

Edit `vars.yml` and change the `user` var:

```yaml
user: kris
```

## Usage

Install everything:

    ansible-playbook -K -v setup.yml

Install certain tags:

    ansible-playbook -K --tags zsh setup.yml

`-K` will prompt for your root/sudo password, if required.

## Notes

There are several sessions which can be selected from the Greeter (login
screen) including Gnome (Ubuntu default) and i3.

## Vagrant/VirtualBox

```
vagrant up --provision
```

## Inspirations

* https://github.com/kalos/ansible-desktop
* https://github.com/chaosmail/dev-env
