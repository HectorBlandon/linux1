```linux
#!/bin/bash

set -e

paramtro= $1

function install_nginx {
yum update
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
}

function install_httpd {
yum update
sudo yum install httpd
sudo systemctl start httpd
sudo systemctl enable httpd
}

function main {

if [ $parametro == "nginx"]
   then 
       echo "instalando nginx"
       #install_nginx
     else
            echo "instalando httpd"
           #install_httpd
}

main
```
