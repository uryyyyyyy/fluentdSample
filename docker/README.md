
## start fluentd

```
gem install fluentd --no-ri --no-rdoc
fluentd --setup ./fluent

# edit fluent.conf
fluentd -c ./fluent/fluent.conf -vv &
```

## client


