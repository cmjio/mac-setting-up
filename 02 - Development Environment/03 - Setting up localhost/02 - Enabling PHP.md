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

## Updating PHP on Mac OS X Mountain Lion

When you want to install the latest version of PHP, or update to the latest verion, then all you have to do is check out this websie, and follow the instructions there: [http://php-osx.liip.ch/](http://php-osx.liip.ch/)

Run the following command if you want to install the latest version of PHP 5.3:<br />
`curl -s http://php-osx.liip.ch/install.sh | bash -s 5.3`

The same goes for PHP 5.4:<br />
`curl -s http://php-osx.liip.ch/install.sh | bash -s 5.4`
