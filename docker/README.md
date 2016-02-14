
## plugin

you can add plugin like this.
```
/opt/td-agent/embedded/bin/fluent-gem install fluent-plugin-s3
```

## config

```
vim /etc/td-agent/td-agent.conf
```

### sample source

```
<source>
  @type http
  port 24224
</source>
```

client can post data like this

```
curl -X POST -d 'json={"json":"message"}' http://172.17.0.2:24224/debug.test
# in this case, "tag" is debug.test
```

### sample out

```
<match debug.*>
  @type stdout
</match>
```

in this case, stdout will be shouwn when tag is `debug.*`.

## start td-agent

```
# on foreground
/usr/sbin/td-agent

# on background
/etc/init.d/td-agent start

```

## client


