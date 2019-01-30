### My Linux Instance for future usage

> Connect to the Linux Instance Using SSH

* Prerequisites:
  * Install an SSH(secure shell) client. Installed by default in mac and linux.
  * Install AWS CLI Tools.
  * Get the instance ID: i-0b04cfd12e3deae28
  * Get the instance DNS name, public DNS(IPV4): 18.224.130.15
  * my private keypair
  * default user name: ec2-user
  
* 要点
  1. 设置好IAM user，给予权限并下载access key id和access key
  2. 设置好aws configure
  3. 在aws console获取instance id之类的信息

* set the permissions of the private key so you can read it: `chmod 400 /path/my-key-pair.pem`
* use `ssh -i /path/my-key-pair.pem ec2-user@ec2-198-51-100-1.compute-1.amazonaws.com` connect to your instance.

> Move file
* `scp -i pemPath filePath ec2-user@awshost:/~` be careful the ec2 instance linux AMI only accept file uploaded to `~`

> 好啦 剩下的就很简单了，去security group，打开3000的端口号，然后就行了
