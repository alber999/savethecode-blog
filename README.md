# SaveTheCode blog

## Author

Alberto Galiana, galiana.alberto@gmail.com

## Overview

This repository contains the **SaveTheCode** blog contents based on [Ghost](https://ghost.org) version 3.

Previously hosted at https://savethecode.com, no longer accessible

Follow instructions below to run the blog in Docker container

## Requirements

Docker installed on your system

## Docker commands

### Run

Create and start container

```
docker run -d --name savethecode-blog \
-e url='http://localhost:3001' \
-e database__client='sqlite3' \
-e database__connection__filename='/var/lib/ghost/content/data/ghost.db' \
-p 3001:2368 \
-v ./content:/var/lib/ghost/content \
ghost:3
```

### Common

Once container exists

```
docker start savethecode-blog
docker stop savethecode-blog
docker rm savethecode-blog
```

## Open blog in browser

Open http://localhost:3001 in your browser
