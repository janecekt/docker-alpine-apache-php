### Overview

* Image based on alpine linux (currnetly 3.6)
* Contains appache 2.4 + php 5.6.30
* Apache runs or port 8080 as user nobody and logs to standard output
* Very low footprint appx 49M


### Build This Image

```
docker build --network=host --tag alpine-apache-php .
```


### Use this image as a base

Copy your php web application into /app/data/htdocs



### Run image

```
docker run -p 8080:8080 alpine-apache-php
```

If you want to store your app on a volume you should start it like so

```
docker run -v /my/volume/:/app/data -p 8080:8080
```
The /my/volume/htdocs should contain your web application