# webtex-dev
[![Build Status](https://travis-ci.org/k3nsuk3/webtex-dev.svg?branch=master)](https://travis-ci.org/k3nsuk3/webtex-dev)
[![](https://images.microbadger.com/badges/image/k3nsuk3/webtex-dev.svg)](https://microbadger.com/images/k3nsuk3/webtex-dev "Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/k3nsuk3/webtex-dev.svg)](https://microbadger.com/images/k3nsuk3/webtex-dev "Get your own version badge on microbadger.com")
[![AMA](https://img.shields.io/badge/ask%20me-anything-0e7fc0.svg)](https://github.com/k3nsuk3/ama)

Developing WebTeX more easier.

#### Before downloading this docker image

1. Fork and clone WebTeX-flask project, rename directory from WebTeX-flask to WebTeX, and change current directory to WebTeX: `$ cd WebTeX`

2. Install Ace.js and RedPen by running below commands

   ````
   $ wget https://github.com/ajaxorg/ace-builds/archive/v1.2.5.tar.gz -O /tmp/ace.tar.gz
   $ mkdir /tmp/ace-builds
   $ tar -xvf /tmp/ace.tar.gz -C /tmp/ace-builds --strip-components 1
   $ mkdir -p WebTeX/static/ace-builds
   $ mv /tmp/ace-builds/src-noconflict WebTeX/static/ace-builds/
   $ rm -f /tmp/ace.tar.gz && rm -rf /tmp/ace-builds

   $ wget https://github.com/redpen-cc/redpen/releases/download/redpen-1.7.6/redpen-1.7.6.tar.gz -O /tmp/redpen.tar.gz
   $ mkdir redpen
   $ tar -xvf /tmp/redpen.tar.gz -C redpen --strip-components 1
   $ rm -f /tmp/redpen.tar.gz
   ````

#### Pull docker image from Docker Hub

```
$ docker pull k3nsuk3/webtex-dev:latest
```

#### Run container from this pulled image
```
$ docker run --rm -it -p 8080:8080 -v /your/developing/WebTeX/path/WebTeX/:/home/user/WebTeX --name container-webtex-dev k3nsuk3/webtex-dev:latest /bin/bash -c "python /home/user/WebTeX/app.py"
```

`-v /foo/bar/WebTeX/WebTeX/:/home/user/WebTeX` if your location of WebTeX app.py is `/foo/bar/WebTeX/WebTeX/app.py`

#### Access WebTeX by your preferred browser

```
http://localhost:8080/
```

#### Sign in to WebTeX by using default user name and password
- Default user name: `Admin`
- Default user password: `webtex`

#### Initial setup of WebTeX
Follow initial setup instruction. Input berow text for each input form.
- User name: Your preferred user name
- User password: Your preferred user password
- JAVA_HOME: `/usr/lib/jvm/java-8-openjdk/jre`
- Absolute path of RedPen configuration file: `/home/user/WebTeX/redpen/conf/redpen-conf-en.xml`

#### Re-login to WebTeX, create working directory, write LaTeX document, and compile

-----

#### Initialize WebTeX.ini and WebTeX.db

```
$ python WebTeX/init.py
```



