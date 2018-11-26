# Import data into MongoDB #

mongoimport --type [json|csv|tsb]

```javascript
mongoimport --db <database> --collection <collection> <data_input_file>
```

## Options ##

### Replace the data if exist insert if not ###

    ```javascript
    mongoimport --upsert --db <database> --collection <collection> <data_input_file>
    ```

### Update missing fields ###

```javascript
mongoimport --upsertFields <field macth> --db <database> --collection <collection> <data_input_file>
```

### Import using csv ###

With Headers in file:

```javascript
mongoimport --type csv --headerline --db <database> --collection <collection> <data_input_file>
```

Without headers in the file:

```javascript
mongoimport --type csv --fields <field_name_1>,<field_name_2>,..,<field_name_n> --db <database> --collection <collection> <data_input_file>
```

With headers file, each header in a new line

```javascript
mongoimport --type csv --fieldFile <path_to_file> --db <database> --collection <collection> <data_input_file>
```
