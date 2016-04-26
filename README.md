<h2>Protecting Apache Web Server from Attacks </h2>
<hr/>

Add the code in your server's httpd.conf file

<ol>
    <li>
        Don't display or send Apache version (Set ServerTokens)
        <pre>
            ServerTokens Prod
        </pre>
    </li>
    <li>
        Don't allow access to .htaccess
        <pre>
            <Directory />
              Options None
              AllowOverride None
              Order allow,deny
              Allow from all
            </Directory>
        </pre>
    </li>
    <li>
        Disable Directory Browsing
        <pre>
            <Directory />
              Options None
              Order allow,deny
              Allow from all
            </Directory>
        </pre>    
            (or)
        <pre>    
            <Directory />
              Options -Indexes
              Order allow,deny
              Allow from all
            </Directory>
        </pre>
    </li>        
    <li>
        Restrict access to root directory (Use Allow and Deny)
        <pre>
          <Directory />
            Options None
            Order deny,allow
            Deny from all
          </Directory>
        </pre>
    </li>
    <li>
        Disable any unnecessary modules
    </li>
    <li>
        Lower the Timeout value to prevent from the ddos attacks
        <pre>
            Timeout 45
        </pre>
    <li>
        Limiting large requests
        <pre>
            LimitRequestBody 1048576
        </pre>
    </li>
    <li>
        Update your OS with the latest patches
    </li>

    <li>
        Disable cgi-bin modules if not needed
    </li>
    <li>
        Update Apache server to the latest version
    </li>
</ol>
