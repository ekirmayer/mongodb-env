# Restore Database #

mongorestore [backup_folder]

```javascript
mongorestore --host <server> --port <port number> <backup_folder>
```

## Complete restore with remove the data from the server ##

```javascript
mongorestore --drop --host <server> --port <port number> <backup_folder>
```

## restore specific collection ##

```javascript
mongorestore --drop --collection <collection name> --db <databse of collection> --host <server> --port <port number> <backup_folder>/<database_backup>/<collection>.bson
```

## Restore with the oplog to the point in time (Only on replicaset) ##

```javascript
mongorestore --oplogReplay <backup_folder>
```