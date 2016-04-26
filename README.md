Protecting Apache Web Server from Attacks

Add the code in your server's httpd.conf file

1. Don't display or send Apache version (Set ServerTokens)
    <CODE>
        ServerTokens Prod
    </CODE>
2. Don't allow access to .htaccess
    CODE => 
            <Directory />
              Options None
              AllowOverride None
              Order allow,deny
              Allow from all
            </Directory>

3. Disable Directory Browsing
  CODE =>  
            <Directory />
              Options None
              Order allow,deny
              Allow from all
            </Directory>
            
            (or)
            
            <Directory />
              Options -Indexes
              Order allow,deny
              Allow from all
            </Directory>

4. Restrict access to root directory (Use Allow and Deny)
  CODE => 
          <Directory />
            Options None
            Order deny,allow
            Deny from all
          </Directory>

5. Disable any unnecessary modules

6. Lower the Timeout value to prevent from the ddos attacks
  CODE => 
    Timeout 45

7. Limiting large requests
  CODE => LimitRequestBody 1048576

8. Update your OS with the latest patches

9. Disable cgi-bin modules if not needed

10. Update Apache server to the latest version

