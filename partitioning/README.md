## partitioning

- why? speed up query
- how? break down large table into smaller chunks
- types
  - horizontal: by rows
    - range: ids, dates
    - list: zip_code, states
    - hash (consistent hashing)
  - vertical: by columns
    - when? separate large columns (blob) out of table
- partitioning vs sharding

| factors     | partitioning                   | sharding                                             |
| ----------- | ------------------------------ | ---------------------------------------------------- |
| physical    | partitions are in same servers | partitions are in diff servers (distributed systems) |
| client      | server job, client agnostic    | client is aware of partitions                        |
| table names | diff table names               | same table name                                      |

## mysql

https://dev.mysql.com/doc/mysql-partitioning-excerpt/5.7/en/partitioning-list.html
