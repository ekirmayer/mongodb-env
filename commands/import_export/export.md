
# Export data from Mongo ##

## Options ##

```javascript
mongoexport --db <database> --collection
```

### Export to file ###

```javascript
mongoexport --db <database> --collection <collection> --out <file>.json
```

### Export specific fields ###

```javascript
mongoexport --db <database> --collection <collection> --fields <filed>,<field>
```

### Export as csv ###

must supply fields when exporting csv

```javascript
mongoexport --db <database> --collection <collection> --fields <filed>,<field> --type=csv
```

### Selective Export ###

```javascript
mongoexport --db <database> --collection <collection> --query <required query>
```

example:

```javascript
mongoexport --db <database> --collection <collection> --query "{_id:{$gt:2}}"
mongoexport --db <database> --collection <collection> --skip 0 --limit 2 --sort "{_id:1}"
```