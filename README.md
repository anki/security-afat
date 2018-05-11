# afat
Script for searching the extracted or mounted firmware file system for items of interest such as:

* etc/shadow and etc/passwd
* list out the etc/ssl directory
* search for SSL and private keys e.g. .pem, .crt, etc.
* search for configuration files
* look for script files
* search for other .bin .fw files
* look for keywords such as admin, password, remote, etc.
* search for common web servers 
* search for common binaries such as ssh, tftp, adbd, dropbear, etc.
* search for URLs, email addresses and IP addresses
* Experimental support for making calls to the Shodan API using the Shodan CLI

## Usage
* 1. make a tmp directory to mount root filesystem `$ mkdir fsmount`
* 2. mount image `$ sudo mount -o loop /home/tt/apq8009-robot-sysfs.img fsmount/`
* 3. Run afat `$ sudo ./afat.sh fsmount/`
* If you wish to use the static code analysis portion of the script, please install eslint: `npm i -g eslint`
* `./afat path to root file system`

## How to extend
* Have a look under 'data' where the checks live or add eslint rules - http://eslint.org/docs/rules/ to eslintrc.json
