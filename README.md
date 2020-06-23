# ProgressivWebApp


Setup webserver on AWS and login via ssh
```
chmod 700 keyFile.pem
ssh -i keyFile.pem ubuntu@awsDNS.com
```

Install relevant packages
```
sudo apt-get install tftp tftpd syslinux apache2
```

Create mount point and copy source
```
sudo mkdir /var/www/html/efs-mount-point
(optional) sudo mount -t efs fs-12345678:/ /var/www/html/efs-mount-point
cd /var/www/html/efs-mount-point 
sudo mkdir sampledir
sudo chown ubuntu sampledir
sudo chmod -R o+r sampledir
sudo mv ~/myPWA sampledir
```

Start webServer
```
sudo systemctl restart apache2
```



