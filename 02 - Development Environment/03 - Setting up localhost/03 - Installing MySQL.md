## Downloading MySQL

1. Go to [MySQL.com > Downloads](http://www.mysql.com/downloads/mysql/).
2. Download the latest version that applies to your system. Login in order to download.

## Installing MySQL

1. Mount the downloaded .dmg file.
2. Install the .pkg file, and then drag the .prefPane file to the System Preferences application to install it, install it for all users.

## Setting up the root user

Start the MySQL server.

`$ cd /usr/local/mysql/bin`<br />
`$ ls -la`<br />
`$ ./mysql -u root # To check if the root password is setup`<br />
`$ exit`<br />
`$ ./mysqladmin -u root password 'rootpwd'`

## Calling mysql commands from anywhere

Add the following to your .bashrc file:

    export PATH="/usr/local/mysql/bin:$PATH"
