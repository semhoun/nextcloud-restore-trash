All thanks goes to [Jan Ackermann](https://github.com/JanAckermann) for his [original script for owncloud](https://github.com/JanAckermann/owncloud-restore-trash).

### Required packages
* php
* composer

### Installation
Run `composer install`

### Run 
Run `php restore.php --url=https://nextcloud.local --username="admin" --password="admin" --date="2022-12-08" --connection=1 --fileregex="/Share/"` \
This might take a while, script can be terminated and restarted any time.

**--url** This is the url of your NextCloud realm \
**--username** This is the username of your NextCloudrealm, only files for this user will be restored \
**--password** This is the password of your NextCloud user \
**--date** This is the date/time since when the lost data will be restored (for example 2022-12-08)  \
**--connections** This is the amount of parallel connections/requests that should be made. I managed to successfully open up to 100 in parallel. This speeds up the script a lot! \
**--fileregex**Regex to match for file restoration (for exemple '/Share/')
