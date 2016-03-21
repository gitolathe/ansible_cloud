# ansible_cloud
Ansible Playbooks for setting up cloud services such as Mesos, Docker and Kubernetes.

To try it out do:

1. Configure `~/.boto` as described in [Boto Config](http://boto.readthedocs.org/en/latest/boto_config_tut.html):

   ```
   [Credentials]
   aws_access_key_id = <your_access_key_here>
   aws_secret_access_key = <your_secret_key_here>
   ```
2. Copy the `ec2.ini`file to `/etc/ansible/ec2.ini`.
3. Add your `*.pem` file to the `ssh-agent`:

   ```
   $ ssh-agent bash 
   $ ssh-add ~/.ssh/keypair.pem 
   ```
3. Run the playbook as `ansible-playbook -i ec2.py -u ubuntu main.yml`.
