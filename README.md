# Vagrant Ansible

Website Dev + Deployment Environment inside of linux OS

This documentation explains the nitty-gritty details and is therefore intended for developers and web-site architects.
It contains the following topics:  

## Prerequisites

To configure Website Dev Environment first you need to install [Vagrant](https://www.vagrantup.com/) and [Oracle VM VirtualBox](https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html)  
knowledge in bash  


## Configuration of the Vagrantfile & ansible

* rename .vlocal.conf.example.yml to .vlocal.conf.yml

## Create virtual machine & SSH to created VM
```Powershell
PS ~/vagrant-imaves> vagrant up
PS ~/vagrant-imaves> vagrant ssh
```

### Create Project
```bash
$ cd /var/www/html
$ composer create-project laravel/laravel project_name
# convenient link from dev user home to site directory
$ sudo ln -s /var/www/html/project_name
```


### git intit inside of shared/project_name
```git
git init
git config core.autocrlf false
//change .gitattributes > * text=off
git add .
git -c user.name='Your name' -c user.email=Your@emailaddres.com commit -m "msg"
git remote add origin 'url'
git push -u origin master
```

## Useful commands:
```Powershell
PS ~/vagrant-imaves> vagrant up/halt/provision/destroy/status
PS ~/vagrant-imaves> vagrant ssh-config
```

## Probable errors:

If windows user profile contains error msg: `incompatible character encodings: CP852 and Windows-1250`  
go to: `C:\HashiCorp\Vagrant\embedded\gems\2.2.19\gems\vagrant-2.2.19\bin\vagrant`

```
#!/usr/bin/env ruby

Encoding.default_external = Encoding.find('Windows-1250')
Encoding.default_internal = Encoding.find('Windows-1250')
```
&  

change Oracle VirtualBox VM location  & adding windows Enviroment Variable VAGRANT_HOME = C:\HashiCorp\Vagrant\.vagrant.d

> Enable-WindowsOptionalFeature -FeatureName ServicesForNFS-ClientOnly, ClientForNFS-Infrastructure -Online -NoRestar

## License
[MIT](LICENSE)

## Author Information
[Mislav Matoković](https://github.com/mmatokovi)
