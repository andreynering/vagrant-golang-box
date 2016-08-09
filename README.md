# vagrant-golang-box

Vagrant box for Go development.

## What is this?

A simple Vagrant box for Golang development.
The idea is having a simple machine that you can use with vanilla Vagrant.
It doesn't depend on Chef, Puppet or any other external plugin.

## Use instructions

- Make sure you have the latests version of [VirtualBox][virtualbox] and [Vagrant][vagrant]
- Download `Vagrantfile` and `vagrant-bootstrap.sh` to your project folder
- Edit the files for your needs/preferences (optional)
- Run `vagrant up`
- When done, login with username `vagrant` and password `vagrant`
- The `GOPATH` environment variable is configured to `~/gopath` (or `/home/vagrant/gopath`)

## Thanks

This repo is inspired by [rails-dev-box][railsdevbox].

[virtualbox]: https://www.virtualbox.org/
[vagrant]: https://www.vagrantup.com/
[railsdevbox]: https://github.com/rails/rails-dev-box
