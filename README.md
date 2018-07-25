# LAMP environment with Docker Compose

## Setup

1. Clone or download this repository.

```
$ git clone https://github.com/tanakaoriginal/docker-compose-lamp-sample.git
$ cd docker-compose-lamp-sample
```

2. Start Services.

```
$ docker-compose up -d
```

3. Create index.php file then access http://localhost:4000/.

```
$ mkdir -p volumes/web/public
$ echo "<?php echo phpinfo();" >> volumes/web/public/index.php
```

4. Access http://localhost:4040/ for PhpMyAdmin.

## Document Root customization

Edit DocumentRoot attribute in `web/conf/00_virtualhost.conf` file.

```
    DocumentRoot "/var/www/html/{YOUR_DESIRED_PATH_IN_WEB_DIR}"
```
