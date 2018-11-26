# Backup Database #

mongodump [destination]

--oplog  => Works only for replic aset

```javascript
mongodump --host <hostname> --port <port number> --out <out folder> --oplog
```

## Backup a specific Database ##

```javascript
mongodump --db <DB Name>
```

## Backup A collection ##

```javascript
mongodump --db <DB Name> --collection <collection name>
```

```javascript
mongodump --username <user for backup> --password <relly good password> --out <outdir>
```

### Note ##

The Admin and Local databases are not backed up by default. Specify the --db flag for back these up when authentication is enabled.