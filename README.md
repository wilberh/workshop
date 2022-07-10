# workshop

ubuntu-20_Jenkins-http_8080

wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get install jenkins

----or----

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

If Jenkins fails to start because a port is in use, run systemctl edit jenkins and add the following:

[Service]
Environment="JENKINS_PORT=8081"




vi /var/log/jenkins/jenkins.log
sudo vi /etc/init.d/jenkins


sudo apt install openjdk-8-jdk
or
sudo apt install openjdk-11-jdk
java --version
javac --version
sudo apt install jenkins
sudo systemctl status jenkins.service
sudo systemctl stop jenkins.service
sudo systemctl start jenkins.service

sudo systemctl status jenkins.service
sudo systemctl activate jenkins.service
sudo systemctl restart jenkins.service
sudo systemctl status jenkins.service
vi /etc/init.d/jenkins 
cat /var/lib/jenkins/secrets/initialAdminPassword
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
sudo systemctl enable jenkins.service


https://tecadmin.net/install-mysql-on-ubuntu-18-04-bionic/
https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04
https://www.linuxshelltips.com/completely-uninstall-mysql-server-in-ubuntu/
sudo apt purge mysql-server*  (fyi - removes binaries and configuration files)
sudo rm -r /etc/mysql /var/lib/mysql
sudo rm -r /var/log/mysql
sudo apt autoremove

https://computingforgeeks.com/how-to-install-mysql-on-ubuntu-focal/
INSTALL VERSION 5.7.38 (on Ubuntu 20.04)-----------------
sudo apt update

sudo apt install wget -y
wget https://dev.mysql.com/get/mysql-apt-config_0.8.12-1_all.deb
sudo dpkg -i mysql-apt-config_0.8.12-1_all.deb
mysql -u root -p
SELECT VERSION();
FLUSH PRIVILEGES;
CREATE USER 'admin'@'localhost' IDENTIFIED BY 'admin';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost';
FLUSH PRIVILEGES;
exit
sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf
(change bind address to 0.0.0.0 to allow remote connections)
sudo systemctl restart mysql

INSTALL LATEST VERSION 8.** ------------------
sudo apt install mysql-server
sudo systemctl start mysql.service
sudo systemctl enable mysql.service

sudo mysql
CREATE USER 'admin'@'localhost' IDENTIFIED BY 'admin';
(or for older systems:
CREATE USER 'admin'@'localhost' IDENTIFIED WITH mysql_native_password BY 'admin';
)
flush privileges;
create database registry_test;
create database registry;
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;
flush privileges;
quit
mysql -u admin -p
sudo mysqladmin -p -u admin version



$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword
27419fa34ebf425480c9c1bcf181ae32

wilberhdez
Password123


courses VM (for virtuabox):
https://www.dropbox.com/s/9cuw54gbx5p6tre/cd-intro1.1.ova?dl=0
or
https://bclconf.s3.us-west-2.amazonaws.com/cd-intro1.1.ova

https://github.com/skilldocs/cd-intro/blob/main/cd-setup.pdf
https://github.com/brentlaster/safaridocs/blob/master/cd-labs.pdf





sudo cat /var/lib/jenkins/secrets/initialAdminPassword
c95d66b35c2d4c43a8876402398e1486


Instance Configuration
Jenkins URL:	
http://ec2-54-173-32-98.compute-1.amazonaws.com:8080/
The Jenkins URL is used to provide the root URL for absolute links to various Jenkins resources. That means this value is required for proper operation of many Jenkins features including email notifications, PR status updates, and the BUILD_URL environment variable provided to build steps.
The proposed default value shown is not saved yet and is generated from the current request, if possible. The best practice is to set this value to the URL that users are expected to use. This will avoid confusion when sharing or viewing links.



