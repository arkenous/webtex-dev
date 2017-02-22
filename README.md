# webtex-dev
[![Build Status](https://travis-ci.org/trileg/webtex-dev.svg?branch=master)](https://travis-ci.org/trileg/webtex-dev)
[![](https://images.microbadger.com/badges/image/trileg/webtex-dev.svg)](https://microbadger.com/images/trileg/webtex-dev "Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/trileg/webtex-dev.svg)](https://microbadger.com/images/trileg/webtex-dev "Get your own version badge on microbadger.com")
[![AMA](https://img.shields.io/badge/ask%20me-anything-0e7fc0.svg)](https://github.com/trileg/ama)

Developing WebTeX more easier.

## How to use?
#### Pull docker image from Docker Hub
```
$ docker pull trileg/webtex-dev:latest
```

#### Run container from this pulled image
```
$ docker run --rm -it -p 8080:8080 -v /your/developing/WebTeX/path/WebTeX/:/home/user/WebTeX --name container-webtex-dev webtex-dev /bin/bash -c "python /home/user/WebTeX/app.py"
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

