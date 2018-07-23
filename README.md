# LAMP environment with Docker Compose

# Setup

1. Replace project name in .env file.

```
PROJECT_NAME=${YOUR_PROJECT_NAME}
```

2. Start Services.

```
$ docker-compose up -d
```

3. Create index.php file then access http://localhost:4000/.

```
$ echo "<?php echo phpinfo();" >> volumes/${YOUR_PROJECT_NAME}/index.php
```

4. Access http://localhost:4040/ for PhpMyAdmin.
