# System-Configuration

Create Virtual Host in LAMP of UBUNTU

/opt/lampp/etc/extra/httpd-vhosts.conf
  <VirtualHost *:80>
  ServerAdmin projectName.local
  DocumentRoot "/opt/lampp/htdocs/Project-Name"
  ServerName projectName.local
  </VirtualHost>

---------------
 etc/hosts
 127.0.0.1	projectName.local
 
 --------------
 /opt/lampp/etc/httpd.conf      //line 487-488
   # Virtual hosts
   Include etc/extra/httpd-vhosts.conf
 =================================================================
 
 Create Virtual Host in Windows

D:\xampp\apache\conf\extra\httpd-vhosts.conf

    <VirtualHost *:80>
    DocumentRoot "D:\xampp/htdocs/Project-Name"
    ServerName Project-Name.local
    <Directory "D:\xampp/htdocs/Project-Name">
    </Directory>
    </VirtualHost>
    
----------------------------------------------

C:\Windows/System32/drivers/etc/hosts

127.0.0.1  Project-Name.local

=================================================================
