# reactConfiguration
Here we are going to setup react app deployment environment, follow the step it will be much ease.
## 1. Installing nodejs
$ sudo yum update
$ sudo yum install nodejs
$ sudo yum install npm

## 2. React environment setup
$ npx create-react-app [app_name]

## 3. Installing MYSQL
$ sudo dnf install mysql-server
> Start mysql service
$ sudo systemctl start mysqld.service
> Checking the status
$ sudo systemctl status mysqld
> Forcing mysql to start whenever you boot server, To stop shift to disable
$ sudo systemctl enable mysqld
#### Securing your MYSQL server
$ sudo mysql_secure_installation
#### Testing MySQL
$ mysqladmin -u root -p version
#### Connecting to your MySQL
$ mysql -u root -p

## 4. Installing httpd
$ sudo yum install httpd
> Forcing apache(httpd) to start whenever you boot server, To stop shift to disable
$ sudo systemctl enable httpd.service
> Start httpd service
$ sudo systemctl start httpd.service
> Open firewall for both http and https
$ sudo firewall-cmd --permanent --add-service=http
> and for https
$ sudo firewall-cmd --permanent --add-service=https
> Reload firewall
$ sudo firewall-cmd --reload
#### Setting Multi-Processing Modules (MPM)
$ sudo httpd -V | grep i mpm
> Before you make the change in your httpd remember to have backup
$ sudo cp /etc/httpd/conf/httpd.conf ~/httpd.conf.backup
