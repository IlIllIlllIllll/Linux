## Linux - Change to Password
### Change to SSH Port in Shell Script - sed
```
sed -i "s|#Port 22|Port <port>|g" /etc/ssh/sshd_config
systemctl restart sshd
```

<br>

### Change to SSH Port in Shell Script - echo
```
echo "Port <port>" >> /etc/ssh/sshd_config
systemctl restart sshd
```