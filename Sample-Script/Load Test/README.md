## ALB Request - Load Test
**Load Test Shell Code**
```shell
#!/bin/bash
ALB_DNS="<ALB DNS>"

while true;
do
    curl -sS http://$ALB_DNS/health
    echo " "
done
```