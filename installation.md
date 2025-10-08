# Installing Jenkinks on Various platforms

## What is Jenkins

Jenkins is a tool that automates the software development process, so code changes can be built, tested, and deployed automatically — without manual effort.

# Available Installaion 

It can be installed on any Platform


# Installaion On Linux 

## Installing On Rhel 

## Create a script which contains the installations commands names **jenkins-install.sh** file 
```bash 
vim jenkins-install.sh
```
Put below in the file
```
wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
 rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
yum upgrade
# Add required dependencies for the jenkins package
yum install fontconfig java-21-openjdk -y
yum install jenkins -y
systemctl daemon-reload
systemctl enable --now jenkins.service

```
## Now change the permission of the file 
```bash 
chmod +x jenkins-install.sh
```
## Run the script 
```bash 
./jenkins-install.sh
```

## Verify the Installaion
```bash 
jenkins --version
```

## Installing On Amazon Linux

## Create a script which contains the installations commands names **jenkins-install.sh** file 
```bash 
vim jenkins-install.sh
```
Put below in the file
```
wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
 rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
yum upgrade
# Add required dependencies for the jenkins package
yum install fontconfig java-21-amazon-corretto -y
yum install jenkins -y
systemctl daemon-reload
systemctl enable --now jenkins.service

```
## Now change the permission of the file 
```bash 
chmod +x jenkins-install.sh
```
## Run the script 
```bash 
./jenkins-install.sh
```

## Verify the Installaion
```bash 
jenkins --version
```
