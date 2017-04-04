# Backup and Restore of MongoDB

> Created by Fisher at 17:42 on 2017-03-12.

## Using mongoexport

```bash
mongoexport --port <port> --db <db-name> --collection <collection-name> --out <out-put-file>


mongoimport --port <port> --db <db-name> --collection <collection-name> --file <to-be-imported-file>
```
