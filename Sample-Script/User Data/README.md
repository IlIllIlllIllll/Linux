## User Data Shell Script
**User Data Shell Code**
```shell
#!/bin/bash
yum update -y
yum install -y jq curl vim
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
ln -s /usr/local/bin/aws /usr/bin/
ln -s /usr/local/bin/aws_completer /usr/bin/
sed -i "s|PasswordAuthentication no|PasswordAuthentication yes|g" /etc/ssh/sshd_config
echo "Port 2222" >> /etc/ssh/sshd_config
systemctl restart sshd
echo '<password>' | passwd --stdin ec2-user
```