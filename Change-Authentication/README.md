## Linux - Authentication on Access
```
sed -i "s|PasswordAuthentication no|PasswordAuthentication yes|g" /etc/ssh/sshd_config
systemctl restart sshd
echo '<password>' | passwd --stdin ec2-user
```

```
echo 'AuthenticationMethods password,publickey' >> /etc/ssh/sshd_config
```

```
systemctl restart sshd
```