# Ansible-Magento 2

This is an ansible playbook to install Magento 2 in a CentOS 8 amazon EC2.
It is installing a Github version of Magento. This version serves the purpose of labing and testing.
If you need to install a production version you may want to change this playbook a bit for that purpose.
It uses Nginx as a web server.

### Magento Documentation for installation
https://devdocs.magento.com/guides/v2.4/install-gde/bk-install-guide.html

### Attention

This is a bare bones installation. Be sure to enforce security good practices on your server and network.

### Requirements

* Brand new Amazon EC2 Amazon Linux, recommended is CentOS08. It may or may not work with other distros.

  * It needs at least 2 GB of Ram.
  
### Installation guide

All variables are inside `group_vars/all.yml`. Take a look and edit following the comments guidance.

Edit file `hosts.yml`, add the AWS EC2 public IP by replacing `AWS_IP` with the IP.

After editing the files, you can run the command:

ansible-playbook -i hosts.yml ansible-magento2.yml -k --private-key ~/.ssh/id_rsa --become

It may take 5 to 10 minutes to finish the installation. 

Thank you.
