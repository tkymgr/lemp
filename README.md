# LEMP skeleton

### Create work folders
```
$ mkdir lemp
$ cd lemp
```

### Deploy from Github
``` 
$ git clone git@github.com:tkymgr/lemp.git .
```

### Create environment file for docker
```
cp env_default .env
```
Feeling to change appropriately after copying.

### Create folders for the environment
```
$ mkdir .data logs app
```
Feel like changing folders according to environment file.

### Create docker images
```
$ docker-compose build
```

### Let's Enjoy!!
```
$ docker-compose up -d
```

