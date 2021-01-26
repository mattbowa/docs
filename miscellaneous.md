
https://cloudcone.com/docs/article/how-to-install-postgresql-11-on-ubuntu-18-04/ -- install postgresql-11-on-ubuntu-18-04/
[REMEMBER the password prompt]
You can now run commands as the PostgreSQL superuser. To create a user, type the following command: createuser --interactive --pwprompt


Install Psycopg2 using the pip command
You should add python requirements used in Postgres on Ubuntu. Run:
sudo apt-get install libpq-dev python-dev
then
pip install psycopg2



https://cloudcone.com/docs/article/how-to-install-pgadmin4-on-ubuntu-18-04/ install pgadmin4-on-ubuntu-18-04/

https://docs.bitnami.com/installer/apps/canvaslms/administration/configure-pgadmin/ --configure server


PSQL Command line
Editing the postgres .configure
sudo vi ./etc/postgresql/12/main/pg_hba.conf
Restarting
sudo /etc/init.d/postgresql restart

loging
psql -d postgres -U  postgres -W

if getting: psql: FATAL:  Peer authentication failed for user "postgres"
by default you would need to use the postgres user:
sudo -u postgres psql postgres

Restarting postgres as root
/etc/init.d/postgresql restart



Stored procedures
https://www.enterprisedb.com/postgres-tutorials/stored-procedures-postgresql-how-create-stored-procedure-and-invoke-it


INSTALLING SAMBA
https://linuxize.com/post/how-to-install-and-configure-samba-on-ubuntu-18-04/


FILE PERMISSIONS
https://www.guru99.com/file-permissions.html


To permanently change your umask you need to update your shell (~/.bashrc), adding umask 000 or whatever
https://geek-university.com/linux/set-the-default-permissions-for-newly-created-files/


Setting up SSH with github
https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh


Installing node
https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04
[better using nvm] https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/

Remove old nodejs installation and update packages.
sudo apt-get remove nodejs npm
sudo apt-get update
sudo apt-get upgrade


#Set up static ip
https://www.howtoforge.com/linux-basics-set-a-static-ip-on-ubuntu

Killing a process on a port
kill $(lsof -t -i:8000)

#Clearing some space for the filesystem:
sudo find /var/log -type f -delete
sudo rm -rf /var/cache/apt/*
sudo apt clean all


#When error hash mismatch when installing docker:
https://stackoverflow.com/questions/61192026/how-do-i-solve-hash-sum-mismatch-on-apt-get-install-docker-ce
