## Downloading phpMyAdmin

1. Go to [phpMyAdmin.net](http://www.phpmyadmin.net)
2. Download the latest version.

## Installing phpMyAdmin

1. Unzip the downloaded .zip file.
2. Move the resulting folder to: ~/Library/WebServer/Documents
3. Rename it to "phpmyadmin".

`$ sudo touch ~/Library/WebServer/Documents/phpmyadmin/config.inc.php`<br />
`$ sudo subl ~/Library/WebServer/Documents/phpmyadmin/config.inc.php`

    <?php
    $i=0;
    $i++;
    $cfg['Servers'][$i]['socket'] = '/tmp/mysql.sock';
    $cfg['Servers'][$i]['user'] = 'root';
    $cfg['Servers'][$i]['password'] = 'rootpwd';
    $cfg['Servers'][$i]['auth_type'] = 'config';
    $cfg['AllowUserDropDatabase'] = 'true';
    ?>