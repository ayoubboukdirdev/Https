# Https
### How to convert your site to https ( Laravel )


:white_check_mark: 1 - Create folder "crt" : C:\xampp\apache

:white_check_mark: 2 - create text file and copy the contents of the makecert.bat file and paste into the text file and rename the name of the file to make-cert.bat

:white_check_mark: 3 - create text file and copy the contents of the cert-template.conf file and paste into the text file and rename the name of the file to cert-template.conf

:white_check_mark: 4 - double click make-cert

:white_check_mark: 5 - 

![https](https://user-images.githubusercontent.com/79239771/123964358-3e224380-d9ab-11eb-86ef-9d29d537cbcd.PNG)

:white_check_mark: 6 - click on the server.crt file 

![https1](https://user-images.githubusercontent.com/79239771/123965688-9a399780-d9ac-11eb-96cd-4b8e0f208451.PNG)

:white_check_mark: 7 - Follow the following steps

![Https2](https://user-images.githubusercontent.com/79239771/123966981-ce618800-d9ad-11eb-803a-f796eb4ed5ae.PNG)

![Https3](https://user-images.githubusercontent.com/79239771/123966993-d28da580-d9ad-11eb-9686-8b8062079f4b.PNG)

![Https4](https://user-images.githubusercontent.com/79239771/123967013-d6b9c300-d9ad-11eb-96cc-9fc74fce4268.PNG)

![Https5](https://user-images.githubusercontent.com/79239771/123967031-dae5e080-d9ad-11eb-9b6b-669c096d3922.PNG)

:white_check_mark: 8 - Head to this path C:\xampp\apache\conf\extra
    :ballot_box_with_check: open this file httpd-vhosts.conf using VS Code
    
    
```bash
         <VirtualHost *:80>
            DocumentRoot "C:/xampp/htdocs/Laravel/test_react/public"
            ServerName test.react
        </VirtualHost>

        <VirtualHost *:443>
            DocumentRoot "C:/xampp/htdocs/Laravel/test_react/public"
            ServerName test.react
            SSLEngine on
            SSLCertificateFile "crt/test.react/server.crt"
            SSLCertificateKeyFile "crt/test.react/server.key"
        </VirtualHost>
   ```
 
  :heavy_check_mark:  DocumentRoot          : Add your project path in htdocs .
  :heavy_check_mark:  SSLCertificateFile    : Add your folder path "crt / domain / server.crt" .
  :heavy_check_mark:  SSLCertificateKeyFile : Add your folder path "crt / domain / server.key" .
  
  :white_check_mark: 9 - go to "C:\Windows\System32\drivers\etc" and open this file Hosts using VS Code 
  
  ```bash
  127.0.0.1       localhost
  ::1             localhost
  
  127.0.0.1       test.react
  ```
  
  :heart_eyes: Thank you ... :heart_eyes:
  
  



