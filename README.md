# Vagrant 

Dev + Deployment Environment 

## Initial config

> Enable-WindowsOptionalFeature -FeatureName ServicesForNFS-ClientOnly, ClientForNFS-Infrastructure -Online -NoRestart

configure .vlocal.conf.yml rename project names

```Powershell
vagrant ssh
```
```bash
cd /var/www/html
```
```bash
composer create-project laravel/laravel project_name
```

### Install Composer
`cd /var/www/html`

composer create-project laravel/laravel project_name

## git intit iside of shared/project_name

git intit
git config core.autocrlf false
git add .
git commit -m ''
git remote add origin 'url'
git push -u orgin master

## After git time for Part 2

remove comments at ansible>main.yml

## Useful commands

```bash
cd /var/www/html
```
```bash
composer create-project laravel/laravel project_name
```

sudo ls /root  
sudo su  
ll  
cd /etc

Service ngnix status/stop/start/restart/reload
vagrant up/halt/provision/suspend/resume
