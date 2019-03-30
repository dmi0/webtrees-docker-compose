# Docker compose for webtrees app

This is a docker compose runner for [webtrees](https://www.webtrees.net/).

## Installation
1. `git clone` it on your server
2. create `.env` file in the same folder and fill it in:
```
WEBTREES_VERSION=1.7.13
PORT=80
MYSQL_ROOT_PASSWORD=put_your_favorite_password
```

  where `WEBTREES_VERSION` is a [webtrees's release](https://github.com/fisharebest/webtrees/releases), `PORT` is web-server exposed port (see bellow), `MYSQL_ROOT_PASSWORD` is mysql database password (see bellow).
  
3. run
```
docker-compose up -d
```
4. Open http://your-server:[PORT] (`PORT` is from .env file) and follow installation instructions. Once you are asked for **Connection to database server** use following values:
  - Server name: database
  - Port number: 3306
  - Database user account: root
  - Database password: [MYSQL_ROOT_PASSWORD]
  
    (where `MYSQL_ROOT_PASSWORD` is from .env file.)
  - All the rest are according to your choice 
  
