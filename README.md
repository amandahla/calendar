## CALENDAR - RADICALE + INFCLOUD + NGINX containers

### PREREQUISITE

#### Environment variables

- RADICALE_DATA_DIR

### HOWTO

### Export environment variable

```bash
export RADICALE_DATA_DIR=~/.var/lib/radicale/collections/
```

#### Change MYUSER in config.js

```javascript
var globalAccountSettings=[
        {
                href: 'http://localhost/radicale/MYUSER/',
                userAuth: {
                        userName: 'MYUSER',
                        userPassword: 'MYUSER'
                }
        }
];
```

#### Runs docker-compose

```bash
docker-compose build
docker-compose up
```

#### Access radicale to create user and calendars

Access URL ```http://localhost/radicale/``` and login with same credentials as set in config.js

#### Access infcloud

Access URL ```http://localhost/```