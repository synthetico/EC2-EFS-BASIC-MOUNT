# EC2-EFS-BASIC-MOUNT
#always update and upgrade your systems 
 sudo yum upgrade     #for Amazon Linux
 sudo yum update -y   # For Amazon Linux
 sudo apt-get update or sudo apt update     # For Debian-based distributions
 
#Insatllation of nfe-utils <br>
sudo yum install -y nfs-utils     # For Amazon Linux or RHEL-based distributions
sudo apt-get install -y nfs-common     # For Debian-based distributions


#Creating a directory <br>
sudo mkdir /mnt/efs<br>

#manually mounting efs to Ec2<br>
sudo mount -t nfs4 -o nfsvers=4.1 <FileSystemID>.efs.<region>.amazonaws.com:/ /mnt/efs<br>

Replace <FileSystemID> with your EFS ID and <region> with your AWS region (e.g., us-east-1).<br>

#Create a file to test the mounted efs<br>

sudo touch /mnt/efs/file.extension  #create a test file and upload to the efs <br>
