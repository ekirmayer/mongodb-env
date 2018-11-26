# Users commands #

## Create User ##

```javascript
use test
db.createUser({user : "test",pwd : "12345",roles: [],
 mechanisms:[  
  "SCRAM-SHA-1",
  "SCRAM-SHA-256"
 ]})
```

## Update User ##

```javascript
use test
db.updateUser("test",{pwd : "12345",roles:[ {"db" : "test", "role":"readWrite"}]})
```