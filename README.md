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
$ sudo systemctl start mysqld.service
$ sudo systemctl status mysqld
$ sudo systemctl enable mysqld // Forcing mysql to start whenever you boot server, To stop shift to disable
#### Securing your MYSQL server
$ 
