## Linux - Change to Password
---
### Change to Password in CentOS
```
sed -i "s|#PasswordAuthentication no|PasswordAuthentication yes|g" /etc/ssh/sshd_config
systemctl restart sshd
echo '<password>' | passwd --stdin ec2-user
```

### Change to Password in ubuntu
```
sed -i "s|#PasswordAuthentication no|PasswordAuthentication yes|g" /etc/ssh/sshd_config
systemctl restart sshd
echo '<ubuntu:password>' | chpasswd
```