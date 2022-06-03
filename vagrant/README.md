# How_to_install_sqlserver_in_ubuntu

refference from [Microsoft Document how to install sqlserver in ubuntu](https://docs.microsoft.com/en-US/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15)
this project has Vagrantfile.

```shell
vagrant up
```

sqlserver-ubuntu environment is being launch.

## AdventureWorks2019 and AdventureWorksDW2019

```shell
# change user and read .bash_profile.
sudo su
source ~/.bash_profile

# execute bash function.
enable_AdventureWorks

# if you drop database, execute below function
disaable_AdventureWorks
```

## WideWorldImporters and WideWorldImportersDW

```shell
# change user and read .bash_profile.
sudo su
source ~/.bash_profile

# execute bash function.
enable_WideWorldImporters

# if you drop database, execute below function
disable_WideWorldImporters
```

## if you want to create vagrant box from vagrant file

```bash
# stop vagrant environment
vagrant halt

# search virtualbox environment.
ls -1 ~/VirtualBox\ VMs/

# packaging your vagrant virtualbox environment. 
vagrant package --base <yourvirtualbox_environment_name> --output ubuntu-sqlserver2019.box

# add box
vagrant box add localhost/ubuntu-sqlserver2019 ubuntu-sqlserver2019.box
```
