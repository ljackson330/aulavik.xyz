1. Install dependencies

```
npm install
```

2. Create OpenRC job

```
#!/sbin/openrc-run

name="Eleventy Server"
description="Runs the 11ty development server"
command="/usr/bin/npx"
command_args="@11ty/eleventy --serve"
command_user="11ty"
directory="/var/www/aulavik.xyz"

pidfile="/var/run/eleventy.pid"
```

3. Start 11ty service

```
rc-service eleventy start
rc-update add eleventy default
```
