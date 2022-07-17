# step 01: Install JAVA

sudo apt-get install openjdk-8-jdk openjdk-8-doc

# step 02: GPG and Repo Key for JFrog Artifactory

sudo apt install wget software-properties-common

wget -qO - https://api.bintray.com/orgs/jfrog/keys/gpg/public.key | apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://jfrog.bintray.com/artifactory-debs $(lsb_release -cs) main"

# step 03: Install JFrog Artofactory

sudo apt update

sudo apt install jfrog-artifactory-oss -y

systemctl start artifactory.service; 

systemctl enable artifactory.service

# Step 04: Access Artifactory Portal

<IP Address>:8081

User name: admin
Password: password


Ref: https://websiteforstudents.com/how-to-install-jfrog-artifactory-on-ubuntu-18-04-16-04/
