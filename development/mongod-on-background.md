# Running mongod on background

Command line option `--fork` can be used to run the MongoDB daemon on background.

```
mongod --fork --dbpath /data/ --logpath /var/log/mongod.log
```

Mongod can also be started as a service
```
sudo service mongod start
```