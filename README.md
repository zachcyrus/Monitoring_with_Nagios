# Monitoring_with_Nagios

## Goal

Implement monitoring of an EC2 Lampstack application through the use of Nagios on a different machine. 

## Steps to replicate 

### Adding SSH Keys to Nagios application

1. SSH into your Nagios instance.
2. Once inside of your Nagios instance utilize the ssh-keygen command to generate public and private key for SSH. Name the file what you want.
   ```
   ssh-keygen -t rsa -b 4096
   ```
   
3. Once the keys are generated, SSH into the the Lamp stack and log into the root.
   ```
   sudo su -
   ```
4. Once logged into the root add the public key of the Nagios instance into the authorized_keys file of the Lamp stack in the .ssh directory.
5. Now go back to your LAMP stack application and attempt to SSH into the root account with your private key.
   ```
   ssh -i nagios_private_key root@private-ip-address
   ```
   
### Install old Ubuntu Repo


### Add Lamptstack to the list of machines to be monitored by Nagios 

1. SSH into your nagios server and change directory to the ncpa_autoregister
   ```
   /usr/local/nagiosxi/scripts/automation/ansible/ncpa_autoregister 
   ```
   
2. 
