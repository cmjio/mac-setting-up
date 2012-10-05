## Enabling PHP on Mac OS X Mountain Lion

Stop the Apache server:<br />
`$ sudo apachectl graceful-stop`

Go to the configuration file:<br />
`$ sudo subl /etc/apache2/httpd.conf`

1. Search for "php".
2. Uncomment the line deactivating PHP, thus activating PHP.
3. Save the changes.

`$ cd /private/etc`<br />
`$ ls php*`<br />
`$ sudo cp php.ini.default php.ini`<br />
`$ sudo subl ./php.ini`

1. Search for "display_errors" twice.
2. Change the value from "Off" to "On".

You can turn Apache on now:<br />
`$ sudo apachectl start`