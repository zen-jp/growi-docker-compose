growi-docker-compose Multiple Sites Example
============================================

This example enables the execution of three GROWI sites.

Install and Start
------------------

### Replace docker-compose.yml
```bash
git clone https://github.com/growilabs/growi-docker-compose.git growi
cd growi
cp examples/multi-app/docker-compose.yml .
```

### Start

```bash
docker-compose up
```

and access to:

* http://localhost:3001 (app-1)
* http://localhost:3002 (app-2)
* http://localhost:3003 (app-3)


Upgrade
-------

### Prepare
```bash
# go to growi-docker-compose workdir
cd growi
```

### Stop

```bash
docker-compose stop
```

### Remove app containers and images
```bash
docker-compose rm app-1
docker-compose rm app-2
docker-compose rm app-3
docker rmi growilabs/growi:7
```

### Pull latest changes
```bash
git pull
cp examples/multi-app/docker-compose.yml .
```

### Start

```bash
docker-compose up
```
