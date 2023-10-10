## Linux
---
### UnInstall Package
**Error**
```
Waiting for process with pid <Process ID> to finish
```
해당 에러는 OutBound에 HTTPS 443이 추가가 안되어 있어 발생하는 에러입니다.

**Trouble-Shooting**
Security Group에 OutBound HTTPS 443이 추가하면 해결됩니다.