## Basic commands

To start apache:<br />
`$ sudo apachectl start`

This will give you a basic Apache server with a DocumentRoot at /Library/WebServer/Documents/

You can enable things like PHP and virtualhosts by making use of the configuration file, which must be edited as root:<br />
`/etc/apache2/httpd.conf`

Restart the apache server (like after editing the config file) with:<br />
`$ sudo apachectl restart`

Stop the Apache server:<br />
`$ sudo apachectl stop`