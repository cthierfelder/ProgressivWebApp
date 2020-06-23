# ProgressivWebApp


ssh -i keyFile.pem ubuntu@awsDNS.com

sudo apt-get install tftp tftpd syslinux apache2
sudo systemctl restart apache2
sudo mkdir /var/www/html/efs-mount-point
???????sudo mount -t efs fs-12345678:/ /var/www/html/efs-mount-point
cd /var/www/html/efs-mount-point 
sudo mkdir sampledir
sudo chown ubuntu sampledir
sudo chmod -R o+r sampledir
cd sampledir
