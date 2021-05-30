# Run MongoDB server and NodeJS at the same time

Add this scripts to **package.json** (mongodb server's path is *data*)

```json
"scripts": {
  "prestart": "mongod --dbpath data --fork --logpath /dev/null",
  "start": "node ./bin/www",
  "poststop": "mongo admin --eval 'db.shutdownServer()' > /dev/null",
  "pretest": "mongod --dbpath data --fork --logpath /dev/null",
  "test": "mocha test",
  "posttest": "mongo admin --eval 'db.shutdownServer()' > /dev/null"
}
```

When executing `npm test` or `npm start`, mongo server will start too.