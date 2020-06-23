# ProgressivWebApp


Setup webserver on AWS and upload source files and login via ssh
```
chmod 700 keyFile.pem
scp -i keyFile.pem myPWA.zip ubuntu@awsDNS.com:
ssh -i keyFile.pem ubuntu@awsDNS.com
```

Install relevant packages
```
sudo apt-get install tftp tftpd syslinux apache2 unzip
```

Unpack source
```
unzip myPWA.zip
```


Create mount point and copy source
```
sudo mkdir /var/www/html/efs-mount-point
(optional) sudo mount -t efs fs-12345678:/ /var/www/html/efs-mount-point
cd /var/www/html/efs-mount-point 
sudo mkdir sampledir
sudo chown ubuntu sampledir
sudo chmod -R o+r sampledir
sudo mv ~/myPWA sampledir/
```

Start webServer
```
sudo systemctl restart apache2
```


![Hello World Screenshot01](./screenshot01.jpg "Hello World Screenshot01")
![Hello World Screenshot02](./screenshot02.jpg "Hello World Screenshot02")
![Hello World Screenshot03](./screenshot02.jpg "Hello World Screenshot03")
