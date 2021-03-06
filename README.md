# Bluz on Homestead

This project is a fork of [laravel/homestead](https://github.com/laravel/homestead) project which allows to use it in a per-project way with [Bluz skeleton](https://github.com/bluzphp/skeleton) application on board.

# How to use

## Requirements

- [Vagrant](https://www.vagrantup.com/) (1.7.2+)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Getting started

1. Clone the repository and run `vagrant up` in the project directory. 
2. After some provisioning you will have 2 ways to access the skeleton application: 
    - through it's IP address - [172.0.13.37:80](http://172.0.13.37)
    - through the port forwarding on your computer - [localhost:8000](http://localhost:8000)

## Database

**bluz-on-homestead** by default creates a database with name `bluz` and credentials `homestead / secret` with fixture data defined in [skeleton](https://github.com/bluzphp/skeleton) project.

## SSH key pairs

By default you login to the virtual machine with command `vagrant ssh`, but sometimes you might need to be authorized here with SSH key pairs.
In this case you need to create SSH key pair and uncomment this lines in `Homestead.yaml`
```
authorize: ~/.ssh/homestead_rsa.pub
keys:
    - ~/.ssh/homestead_rsa
```
More information you can find in the official [documentation](#Documentation) of original project.

## Ports

The following ports are forwarded to your Homestead environment:

- HTTP: 8000 -> Forwards To 80
- MySQL: 33060 -> Forwards To 3306
- Postgres: 54320 -> Forwards To 5432

[http://laravel.com/docs/homestead#ports](http://laravel.com/docs/4.2/homestead#ports)

## Blackfire

... TBD ...

# F.A.Q.

... TBD ...

# Documentation 

Full official documentation of original Homestead project [is located here](http://laravel.com/docs/homestead).