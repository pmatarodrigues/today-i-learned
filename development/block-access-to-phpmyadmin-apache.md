# Block access to phpMyAdmin in Apache 


Change the file `/etc/httpd/conf.d/phpmyadmin.conf/`:
Remove comments to allow access.

`
<Directory /usr/share/phpMyAdmin/>
   <IfModule mod_authz_core.c>
     # Apache 2.4
     <RequireAny>
      Require ip 127.0.0.1
      Require ip ::1
	    #Require all granted
     </RequireAny>
   </IfModule>
   <IfModule !mod_authz_core.c>
     # Apache 2.2
     Order Deny,Allow
     Deny from All
     #Allow from All
     Allow from 127.0.0.1
     Allow from ::1
   </IfModule>
</Directory>

`