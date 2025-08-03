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

# Enable xDebug for Windows with VS code

  1. Create a details.php file in your project and paste the code:-

            <?php
               phpinfo();
            ?>

  2. Run on crome to see the all details and copy all the details(ctrl+A).
  3. Go to https://xdebug.org/wizard paste into the installation wizard and click on btn "Analyse my phpinfo() output"
  4. From Instructions: Download the file and Move the downloaded file to C:\xampp\php\ext.
  5. Update C:\xampp\php\php.ini to below lines of code.
     
            zend_extension="C:\xampp\php\ext\Downloaded FILE Name"
            xdebug.mode=debug
            xdebug.start_with_request=yes
            xdebug.client_port=9003
            xdebug.client_host=127.0.0.1
     
  6. Restart the Apache Webserver.
  7. Run the command on terminal

          php -v
     
  8. and check output like below:
    PHP 8.2.12 (cli) (built: Oct 24 2023 21:15:15) (ZTS Visual C++ 2019 x64)
    Copyright (c) The PHP Group
    Zend Engine v4.2.12, Copyright (c) Zend Technologies
        with Xdebug v3.4.5, Copyright (c) 2002-2025, by Derick Rethans

  9. Then Install PHP Debug Extension in VS Code
      Go to the Extensions view (Ctrl+Shift+X)
      Search for "PHP Debug" by Felix Becker (or search by the Extension ID as well)

         xdebug.php-debug
     
      Click to Install.

  10. Create launch.json in VS Code
        Open the Run and Debug panel (Ctrl+Shift+D)
        Click "create a launch.json file"
        Choose PHP
        VS Code will generate a default config like this:

          {
            // Use IntelliSense to learn about possible attributes.
            // Hover to view descriptions of existing attributes.
            // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
            "version": "0.2.0",
            "configurations": [
                
                {
                    "name": "Listen for Xdebug",
                    "type": "php",
                    "request": "launch",
                    "port": 9003
                },
                {
                    "name": "Launch currently open script",
                    "type": "php",
                    "request": "launch",
                    "program": "${file}",
                    "cwd": "${fileDirname}",
                    "port": 0,
                    "runtimeArgs": [
                        "-dxdebug.start_with_request=yes"
                    ],
                    "env": {
                        "XDEBUG_MODE": "debug,develop",
                        "XDEBUG_CONFIG": "client_port=${port}"
                    }
                },
                {
                    "name": "Launch Built-in web server",
                    "type": "php",
                    "request": "launch",
                    "runtimeArgs": [
                        "-dxdebug.mode=debug",
                        "-dxdebug.start_with_request=yes",
                        "-S",
                        "localhost:0"
                    ],
                    "program": "",
                    "cwd": "${workspaceRoot}",
                    "port": 9003,
                    "serverReadyAction": {
                        "pattern": "Development Server \\(http://localhost:([0-9]+)\\) started",
                        "uriFormat": "http://localhost:%s",
                        "action": "openExternally"
                    }
                }
            ]
          }

  11. Now once close the VS code and reopen and Set Breakpoints and Start Debugging "Enjoy".
      


    
