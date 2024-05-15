# Maven-installation

HOW TO INSTALL MAVEN FOR USE AS A BUILD TOOL

Install Java JDK 1.8+ and other softares (GIT, wget and tree)

# install Java JDK 1.8+ as a pre-requisit for maven to run.

sudo hostnamectl set-hostname maven

sudo su - ec2-user

cd /opt

sudo yum install wget nano tree unzip git-all -y

sudo yum install java-11-openjdk-devel java-1.8.0-openjdk-devel -y

java -version

git - version

2. Download, extract and Install Maven
   
#Step1) Download the Maven Software

sudo wget https://dlcdn.apache.org/maven/maven-3/3.9.0/binaries/apache-maven-3.9.0-bin.zip

sudo unzip apache-maven-3.9.0-bin.zip

sudo rm -rf apache-maven-3.9.0-bin.zip

sudo mv apache-maven-3.9.0/ maven

.#Step3) Set Environmental Variable - For Specific User eg ec2-user

vi ~/.bash_profile # and add the lines below

export M2_HOME=/opt/maven

export PATH=$PATH:$M2_HOME/bin

.#Step4) Refresh the profile file and Verify if maven is running

source ~/.bash_profile

mvn -version

